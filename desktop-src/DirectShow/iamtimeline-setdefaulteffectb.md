---
description: 'Метод Сетдефаултеффектб задает результат по умолчанию. Этот метод эквивалентен Иамтимелине:: Сетдефаултеффект, но принимает значение BSTR, а не указатель на GUID.'
ms.assetid: ffee9728-f69e-48a4-ac0a-d41347a20deb
title: 'Метод Иамтимелине:: Сетдефаултеффектб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a8722a195078cb032285e4ea2ac449ad045d54f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651781"
---
# <a name="iamtimelinesetdefaulteffectb-method"></a>Метод Иамтимелине:: Сетдефаултеффектб

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetDefaultEffectB`Метод задает результат по умолчанию. Этот метод эквивалентен [**иамтимелине:: сетдефаултеффект**](iamtimeline-setdefaulteffect.md), но принимает значение BSTR, а не указатель на GUID.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDefaultEffectB(
   BSTR pGuid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуид* 
</dt> <dd>

Значение BSTR, представляющее идентификатор GUID для действия по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелине**](iamtimeline.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




