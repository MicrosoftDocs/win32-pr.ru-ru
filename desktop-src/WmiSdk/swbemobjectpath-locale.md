---
description: Свойство Locale объекта Свбемобжектпас содержит языковой стандарт пути к объекту.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Свойство Свбемобжектпас. locale (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693264"
---
# <a name="swbemobjectpathlocale-property"></a>Свбемобжектпас. locale, свойство

Свойство **locale** объекта [**свбемобжектпас**](swbemobjectpath.md) содержит языковой стандарт пути к объекту.

Если свойство **свбемобжектпас. locale** является частью автономного объекта [**свбемобжектпас**](swbemobjectpath.md) , оно доступно для чтения и записи и может использоваться для установки компонента языкового стандарта моникера.

Если доступ к свойству **свбемобжектпас. locale** осуществляется как часть свойства [**SWbemObject. Path \_**](swbemobject-path-.md) , он доступен только для чтения и сообщает значение локали, используемое в привязке к пространству имен, из которого был получен объект.

Для идентификаторов языковых стандартов Майкрософт формат строки — MS \_ XXXX, где XXXX — строка в шестнадцатеричном формате, указывающая код языка. Например, идентификатором английского языка (США) является "MS \_ 409".

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМОБЖЕКТПАС CLSID<br/>                                                       |
| IID<br/>                      | IID \_ исвбемобжектпас<br/>                                                        |



 

 




