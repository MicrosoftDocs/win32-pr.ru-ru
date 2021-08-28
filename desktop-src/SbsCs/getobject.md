---
description: Метод GetObject возвращает экземпляр существующего объекта Microsoft. Windows. Объект Акткткс.
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
ms.openlocfilehash: b6c47c00f50cdeaa97fd0fafcd8aefa3c4863bc1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886616"
---
# <a name="actctxgetobject-method"></a>Акткткс. GetObject, метод

Метод **GetObject** возвращает экземпляр существующего объекта [**Microsoft. Windows. Объект Акткткс**](microsoft-windows-actctx-object.md) .

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

Обязательная строка, указывающая на объект. имя должно быть в реестре в разделе **HKEY \_ локальный \_ компьютер** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **&lt; пакетная &gt;** \\ **автоматизация**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ иакткткс определен как 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Метод CreateObject**](createobject.md)
</dt> </dl>

 

 




