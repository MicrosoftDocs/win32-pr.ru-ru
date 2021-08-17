---
description: В структуре "сведения о ПОРТе 2" указан \_ \_ поддерживаемый порт принтера.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: Структура PORT_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 053745ff90e022ef2ed466518a9210d6dde18d3562fdb4232d9f4d262460ea7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470944"
---
# <a name="port_info_2-structure"></a>\_Сведения о порте \_ 2 Структура

В структуре " **\_ сведения о порте \_ 2** " указан поддерживаемый порт принтера.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a>Члены

<dl> <dt>

**ппортнаме**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая определяет поддерживаемый порт принтера (например, "LPT1:").

</dd> <dt>

**пмониторнаме**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая определяет установленный монитор (например, "монитор PJL"). Может иметь **значение NULL**.

</dd> <dt>

**пдескриптион**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая более подробно описывает порт (например, если **ппортнаме** имеет значение LPT1:, **пдескриптион** — "порт принтера"). Может иметь **значение NULL**.

</dd> <dt>

**фпорттипе**
</dt> <dd>

Битовая маска, описывающая тип порта. Этот элемент может быть сочетанием следующих значений:

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**\_запись типа \_ порта**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**\_Чтение типа \_ порта**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**\_ПЕРЕнаправленный тип порта \_**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**\_тип порта \_ \_ подключен к сети**
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Процессу должно быть равно нулю.

</dd> </dl>

## <a name="remarks"></a>Remarks

Используйте структуру **порт \_ \_ 2** при вызове [**енумпортс**](enumports.md) , если установлено несколько мониторов, поддерживающих одни и те же порты.

Элемент **фпорттипе** можно запросить для определения сведений о порте. Обратите внимание, что параметры порта не влияют на атрибуты принтера (как они возвращаются элементом **Attributes** [**\_ сведений о принтере \_ 2**](printer-info-2.md)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ \_ Сведения о \_ порте 2W** (Юникод) и **\_ \_ сведения о порте \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




