---
description: Свойство Parameters объекта Свбеммесод — это объект SWbemObject, свойства которого определяют выходные параметры и тип возвращаемого значения этого метода. Это свойство доступно только для чтения.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: Свойство Свбеммесод. parameters (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2087dd545a37cdc4b82899cb261cfef5fdb1fda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693221"
---
# <a name="swbemmethodoutparameters-property"></a>Свбеммесод. Parameters, свойство

Свойство **Parameters** объекта [**свбеммесод**](swbemmethod.md) — это объект [**SWbemObject**](swbemobject.md) , свойства которого определяют выходные параметры и тип возвращаемого значения этого метода. Это свойство доступно только для чтения.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Дополнительные сведения об использовании этого свойства для получения выходных параметров из методов поставщика см. в разделе [конструирование объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Обратите внимание, что любые изменения, внесенные в этот объект, не отражаются в определении базового метода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕММЕСОД CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбеммесод<br/>                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбеммесод**](swbemmethod.md)
</dt> <dt>

[**SWbemObject.ExeКмесод\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExeКмесодасинк\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExeКмесод**](swbemservices-execmethod.md)
</dt> <dt>

[**SWbemServices.ExeКмесодасинк**](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




