---
title: Метод WSMan. Креатересаурцелокатор (Всмандисп. h)
description: Создает объект ResourceLocator, который можно использовать вместо указания URI ресурса в операциях с объектами сеанса, таких как Session. Get, Session. Where или Session. Enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Креатересаурцелокатор
- Служба удаленного управления Windows метода Креатересаурцелокатор, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Креатересаурцелокатор
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988568"
---
# <a name="wsmancreateresourcelocator-method"></a>Метод WSMan. Креатересаурцелокатор

Создает объект [**ResourceLocator**](resourcelocator.md) , который можно использовать вместо указания URI ресурса в операциях с объектами [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*универсальный код ресурса* \[ в необязательное\]
</dt> <dd>

URI ресурса для ресурса. Дополнительные сведения о строках URI см. в разделе [URI ресурсов](resource-uris.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект [**ResourceLocator**](resourcelocator.md) , который затем можно использовать для выполнения локальных или удаленных операций WinRM.

## <a name="remarks"></a>Комментарии

Если свойство **фрагментдиалект** не указано в объекте [**ResourceLocator**](resourcelocator.md) , по умолчанию используется спецификация XPath 1,0. Дополнительные сведения см. на веб-сайте [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="examples"></a>Примеры

Следующий пример кода VBScript создает объект [**ResourceLocator**](resourcelocator.md) и получает значение свойства **Description** сетевого адаптера из экземпляра [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) с индексом "1".


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**Session**](session.md)
</dt> </dl>

 

