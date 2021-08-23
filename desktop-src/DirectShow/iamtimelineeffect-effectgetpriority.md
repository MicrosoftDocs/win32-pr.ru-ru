---
description: Метод Еффектжетприорити извлекает уровень приоритета результата. Для данного объекта механизм визуализации применяет эффекты в порядке приоритета, начиная с нулевого уровня приоритета.
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: 'Метод Иамтимелиниффект:: Еффектжетприорити (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect.EffectGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 62a66024961d0b36b0706510754092e1da3a9e7c6bc72bee6bc9c9b0dacf3187
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812394"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a>Метод Иамтимелиниффект:: Еффектжетприорити

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`EffectGetPriority`Метод получает уровень приоритета результата. Для данного объекта механизм визуализации применяет эффекты в порядке приоритета, начиная с нулевого уровня приоритета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pVal* 
</dt> <dd>

Получает уровень приоритета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелиниффект**](iamtimelineeffect.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




