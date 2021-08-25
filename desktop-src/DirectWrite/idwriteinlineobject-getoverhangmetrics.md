---
title: Идвритеинлинеобжект Жетоверхангметрикс, метод
description: Идвритетекстлайаут вызывает эту функцию обратного вызова для получения видимых экстентов (в DIP) встроенного объекта. В случае с простым точечным рисунком без заполнения и без выступа все перевисает просто будут обнулены.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Непосредственная запись метода Жетоверхангметрикс
- Прямая запись метода Жетоверхангметрикс, интерфейс Идвритеинлинеобжект
- Прямая запись интерфейса Идвритеинлинеобжект, метод Жетоверхангметрикс
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 011794fc3804435dd565a00035247436814c41474c60b66f90c5cb5d9594f6c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928154"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>Метод Идвритеинлинеобжект:: Жетоверхангметрикс

[**Идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) вызывает эту функцию обратного вызова для получения видимых экстентов (в DIP) встроенного объекта. В случае с простым точечным рисунком без заполнения и без выступа все перевисает просто будут обнулены.

Перестает возвращаться по отношению к сообщаемому размеру объекта (см. раздел [**ДВРИТЕ \_ inline \_ Object \_ метрики**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) и не должен быть скорректирован в базовом плане.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*перестает отвечать* \[ заполняет\]
</dt> <dd>

Тип: **[ **двритеные \_ \_ метрики выступа**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Отклонение видимых экстентов (в DIP-параметрах) за пределами объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Дврите. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**идвритеинлинеобжект**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**идвритеинлинеобжект**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

