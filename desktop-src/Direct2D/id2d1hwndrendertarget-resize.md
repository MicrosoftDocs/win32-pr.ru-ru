---
title: Методы изменения размера ID2D1HwndRenderTarget (D2d1. h)
description: Изменяет размер целевого объекта отрисовки на указанный размер в пикселях.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Методы изменения размера Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 31ffcae6473924e12ca428fd48927fd1507840dce4fdbce3a18e8f82ffe9fcaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917614"
---
# <a name="id2d1hwndrendertargetresize-methods"></a>Методы ID2D1HwndRenderTarget:: resize

Изменяет размер целевого объекта отрисовки на указанный размер в пикселях.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                         | Описание                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Изменение размера (D2D1 \_ size \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))  | Изменяет размер целевого объекта отрисовки на указанный размер в пикселях. <br/> |
| [**Изменить размер (D2D1 \_ размер \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) | Изменяет размер целевого объекта отрисовки на указанный размер в пикселях.<br/>  |



## <a name="remarks"></a>Remarks

После вызова этого метода содержимое заднего буфера целевого объекта прорисовки не определяется, даже если при создании целевого объекта отрисовки был указан параметр [**D2D1 \_ Present \_ Options ( \_ хранить \_ содержимое**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) ).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))
</dt> </dl>

�

�
