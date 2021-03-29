---
description: Метод GetObject возвращает экземпляр существующего объекта Microsoft. Windows. Акткткс.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: Акткткс. GetObject, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809371"
---
# <a name="actctxgetobject-method"></a>Акткткс. GetObject, метод

Метод **GetObject** возвращает экземпляр существующего объекта [**Microsoft. Windows. акткткс**](microsoft-windows-actctx-object.md) .

## <a name="syntax"></a>Синтаксис


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*bstrName* 
</dt> <dd>

Обязательная строка, указывающая на объект. Имя должно быть в реестре в разделе **hKey \_ локальный \_ компьютер** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ иакткткс определен как 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Метод CreateObject**](createobject.md)
</dt> </dl>

 

 




