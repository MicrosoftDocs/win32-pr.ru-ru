---
title: Метод Controls. Step
description: Метод Step заставляет текущий видеоматериал закреплять воспроизведение на следующем кадре или предыдущем кадре.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- проигрыватель Windows Media метода step
- метод step проигрыватель Windows Media, класс controls
- класс элементов управления проигрыватель Windows Media, метод step
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4626ff80aee55ad6c22be7580a07ef2319afb6792a8c11b815d72af23b5727fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839829"
---
# <a name="controlsstep-method"></a>Метод Controls. Step

Метод **Step** заставляет текущий видеоматериал закреплять воспроизведение на следующем кадре или предыдущем кадре.

## <a name="syntax"></a>Синтаксис


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фрамекаунт* \[ окне\]
</dt> <dd>

**Число** (**длинное**), указывающее, сколько кадров следует пошагово перед замораживанием. В настоящее время необходимо задать значение 1 или-1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

В настоящее время этот метод поддерживает только параметры 1 или-1, поэтому каждый раз можно пошаговым образом выполнять только один кадр.

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media для Windows XP или более поздней версии.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Объект DVD**](dvd-object.md)
</dt> </dl>

 

 





