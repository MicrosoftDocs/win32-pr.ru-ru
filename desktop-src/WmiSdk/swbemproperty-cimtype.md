---
description: Свойство Цимтипе объекта SWbemProperty — это целое число, которое можно использовать для определения типа CIM этого свойства. Это свойство доступно только для чтения.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Свойство SWbemProperty. Цимтипе (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998664"
---
# <a name="swbempropertycimtype-property"></a>SWbemProperty. Цимтипе, свойство

Свойство **Цимтипе** объекта [**SWbemProperty**](swbemproperty.md) — это целое число, которое можно использовать для определения типа CIM этого свойства. Это свойство доступно только для чтения.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Дополнительные сведения о допустимых типах для этого свойства см. в разделе [**вбемЦимтипинум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).

Экземпляры внедренных объектов хранятся в составных объектах в виде свойств типа **\_ объекта CIM**. Чтобы определить класс внедренного объекта в экземпляре составного класса, необходимо изучить квалификатор **Цимтипе** свойства типа **\_ объекта CIM** .

Ссылки на объекты в классе ассоциации хранятся в свойствах типа " **\_ ссылка на CIM**". Чтобы определить фактические пути к объекту, необходимо проверить квалификатор **Цимтипе** свойства **\_ ссылочного типа CIM** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTY CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемпроперти<br/>                                                          |



 

 




