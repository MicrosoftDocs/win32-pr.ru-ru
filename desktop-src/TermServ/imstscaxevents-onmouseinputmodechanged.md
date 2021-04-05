---
title: Имстскаксевентс Онмаусеинпутмодечанжед, метод
description: Вызывается при изменении режима ввода с помощью мыши.
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онмаусеинпутмодечанжед
- Службы удаленных рабочих столов метода Онмаусеинпутмодечанжед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онмаусеинпутмодечанжед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnMouseInputModeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbfef19aa79ba634a13d92b8d11866b8016e893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136326"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a>Метод Имстскаксевентс:: Онмаусеинпутмодечанжед

Вызывается при изменении режима ввода с помощью мыши.

## <a name="syntax"></a>Синтаксис


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фмаусемодерелативе* \[ окне\]
</dt> <dd>

Указывает, находится ли указатель мыши в относительном режиме.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что режим ввода мыши изменился.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





