---
description: Метод Клоседатабасе объекта Merge закрывает текущую открытую установщик Windows базу данных.
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
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674781"
---
# <a name="mergeclosedatabase-method"></a>Метод Merge. Клоседатабасе

Метод **клоседатабасе** объекта [**Merge**](merge-object.md) закрывает текущую открытую установщик Windows базу данных.

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

## <a name="remarks"></a>Комментарии

При закрытии базы данных удаляются все сведения о зависимостях, но не затрагиваются все ошибки, которые не были получены.

### <a name="c"></a>C++

См. раздел Функция [**клоседатабасе**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
