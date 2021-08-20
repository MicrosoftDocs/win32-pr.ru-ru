---
description: метод клоседатабасе объекта Merge закрывает текущую открытую установщик Windows базу данных.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Метод Merge. Клоседатабасе (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3f3b250cbaebd565f14ef7f10cd8180e497f20347d00a7e96a74298d3e5dc770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013032"
---
# <a name="mergeclosedatabase-method"></a>Метод Merge. Клоседатабасе

метод **клоседатабасе** объекта [**Merge**](merge-object.md) закрывает текущую открытую установщик Windows базу данных.

## <a name="syntax"></a>Синтаксис


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бкоммит* 
</dt> <dd>

**Значение true** , если необходимо сохранить изменения; в противном случае — **значение false** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

При закрытии базы данных удаляются все сведения о зависимостях, но не затрагиваются все ошибки, которые не были получены.

### <a name="c"></a>C++

См. раздел Функция [**клоседатабасе**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Заголовок<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
