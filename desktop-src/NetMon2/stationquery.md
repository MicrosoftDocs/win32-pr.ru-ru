---
description: Структура СТАТИОНКУЕРИ предоставляет сведения о конкретном компьютере, использующем сетевой монитор.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: Структура СТАТИОНКУЕРИ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de76c4da7bc27d76c04aeeaa7a46d69134e411ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673539"
---
# <a name="stationquery-structure"></a>Структура СТАТИОНКУЕРИ

Структура **статионкуери** предоставляет сведения о конкретном компьютере, использующем сетевой монитор.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a>Члены

<dl> <dt>

**Флаги**
</dt> <dd>

Флаги, которые указывают текущее состояние сетевой монитор.



| Значение                                                                                                                                                                                                                | Значение                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <dt>**\_Флаги статионкуери \_ загружены**</dt> </dl>                   | Драйвер загружен, но не является ядром.<br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <dt>**СТАТИОНКУЕРИные \_ Флаги \_**</dt> </dl>                | Драйвер загружен, но не захватывает данные.<br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <dt>**\_захват флагов статионкуери \_**</dt> </dl>          | Драйвер активно вовлечен в захват.<br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <dt>**\_Передача флагов статионкуери \_**</dt> </dl> | Этот флаг устарел.<br/>                       |



 

</dd> <dt>

**бкдверминор**
</dt> <dd>

Дополнительный номер версии сетевой монитор, установленного на компьютере.

</dd> <dt>

**бкдвермажор**
</dt> <dd>

Основной номер версии сетевой монитор, установленной на компьютере.

</dd> <dt>

**лиценсенумбер**
</dt> <dd>

Номер лицензии на программное обеспечение.

</dd> <dt>

**MachineName**
</dt> <dd>

Имя изготовителя компьютера (при наличии).

</dd> <dt>

**UserName**
</dt> <dd>

Имя пользователя или идентификатор системы.

</dd> <dt>

**Reserved**
</dt> <dd>

Зарезервировано для последующего использования.

</dd> <dt>

**адаптераддресс**
</dt> <dd>

Адрес сетевой карты.

</dd> <dt>

**вмачиненаме**
</dt> <dd>

Имя компьютера в Юникоде. Этот элемент применяется к сетевой монитор 2,0 или более поздней версии.

</dd> <dt>

**вусернаме**
</dt> <dd>

Имя пользователя в Юникоде. Этот элемент применяется к сетевой монитор 2,0 или более поздней версии.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Массив этих структур используется структурой [куеритабле](querytable.md) для предоставления списка компьютеров, которые в настоящее время используют сетевой монитор для сбора данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[куеритабле](querytable.md)
</dt> </dl>

 

 




