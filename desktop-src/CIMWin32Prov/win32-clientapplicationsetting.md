---
description: '\_Класс WMI взаимосвязей Win32 клиентаппликатионсеттинг связывает исполняемый файл и приложение модели COM, которое содержит параметры конфигурации COM для исполняемого файла.'
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Класс Win32_ClientApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 359478d7cf6069e17ae02358f4ea48ffc44169f6822f4f8b3e33dad332fab020
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546374"
---
# <a name="win32_clientapplicationsetting-class"></a>\_Класс Win32 клиентаппликатионсеттинг

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ клиентаппликатионсеттинг** связывает исполняемый файл и приложение модели COM, которое содержит параметры конфигурации COM для исполняемого файла.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ клиентаппликатионсеттинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ клиентаппликатионсеттинг** имеет следующие свойства.

<dl> <dt>

**Приложение**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ дкомаппликатион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ дкомаппликатион")
</dt> </dl>

Ссылка на экземпляр, представляющий COM-приложение, которое содержит параметры конфигурации исполняемого файла.

</dd> <dt>

**Клиент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ File**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ File")
</dt> </dl>

Ссылка на экземпляр, представляющий исполняемый файл, использующий параметры COM.

</dd> </dl>

## <a name="remarks"></a>Remarks

**Win32 \_ Клиентаппликатионсеттинг** не поддерживает перечисление.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

