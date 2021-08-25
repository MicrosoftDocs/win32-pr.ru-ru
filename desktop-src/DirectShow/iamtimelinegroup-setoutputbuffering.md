---
description: Метод Сетаутпутбуфферинг задает число кадров, отображаемых заранее во время просмотра.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'Метод Иамтимелинеграуп:: Сетаутпутбуфферинг (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8187918a4f6d04df9c8c0eaff387a092f18181071ce6ba41c83de44fcb095bbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915194"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a>Метод Иамтимелинеграуп:: Сетаутпутбуфферинг

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetOutputBuffering`Метод задает число кадров, отображаемых заранее во время просмотра.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*нбуффер* \[ окне\]
</dt> <dd>

Число кадров в буфере во время предварительной версии. Должно быть два или более.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Буфер большего размера требует больше памяти, но может привести к более гладкому просмотру, особенно во время эффектов или переходов, требующих больше времени для отрисовки. Буфер по умолчанию — 30 кадров.

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

[**Интерфейс Иамтимелинеграуп**](iamtimelinegroup.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




