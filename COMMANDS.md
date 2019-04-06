# Команды

## Использование

### Монитор порта Arduino

Запускать от **Администратора**!

Параметры соединения:
57600 бод
NL (Новая строка)

Для установки соединения:
*knock*

## Режимы

***mode** get*

***mode** set* {full|safe}

## Движения

***go*** {what} {where} {time} {notify}
	return move

***move*** {what} {where} {time} после этой команды обязательно использовать *commit*

***commit*** {notify}

***done***

## Разное

***hello***
	hi

***knock***
	knock who's there

***init_state***
	finished or current step

## Конфигурация

***config** get* {motor} motor=id
	id start offset reversed min max pin

***config** from_motors* {offset}

***config** set* motor {id} {key} {value} [1] после нужно выполнить save и fix
		key := start | offset | reversed | min | max | pin

***config** save* [2]
	запись конфигурации в хранилище


***config** fix* [3]
	если на этапе инициализации конфигурация не прошла валидацию

***crc***
	OBJECT_CRC(config));
***break***
	break_storage_config()


# Параметры сервоприводов

## Start
	print("returning to start")
        self.move(1, 0, 2000)
        self.move(6, 0, 2000)
        self.move(2, -80, 2000)
        self.move(7, -80, 2000)
        self.move(3, 0, 2000)
        self.move(8, 0, 2000)
        self.commit()
        self.wait_for_done(6)
        print("returning to start..done")

## Sit down
    def sit_down(self, D, time=2000, block=True):
        """
        Should be done from standing position
        """
        print("sitting down")
        self.move(1, D, time)
        self.move(6, D, time)
        self.move(2, -80 + 2 * D, time)
        self.move(7, -80 + 2 * D, time)
        self.move(3, -D - 10, time)
        self.move(8, -D - 10, time)
        if block:
            self.commit()
            self.wait_for_done(8)
            print("sitting down..done")
