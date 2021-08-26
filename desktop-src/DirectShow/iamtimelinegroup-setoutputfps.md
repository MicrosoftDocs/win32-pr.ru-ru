---
description: Метод Сетаутпутфпс задает несжатую частоту выходного кадра для этой группы.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'Метод Иамтимелинеграуп:: Сетаутпутфпс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 332e9ea33e0ca559800e560409066946247d1cff34b8e6b48fd1fadbdb91e38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052705"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a>Метод Иамтимелинеграуп:: Сетаутпутфпс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetOutputFPS`Метод задает несжатую частоту выходного кадра для этой группы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Кадры в секунду* 
</dt> <dd>

Частота вывода кадров для этой группы, в кадрах в секунду. Значение не может равняться нулю и не может содержать более семи цифр после десятичного знака.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Отображаемые выходные данные этой группы выполняются с заданной частотой кадров, и все изменения в исходном материале округляются до ближайшей границы фрейма, как определено частотой кадров. Для лучшей производительности используйте одинаковую частоту кадров для всех групп, видео и аудио.

Метод [**иамтимелинеграуп:: сетсмартрекомпрессформат**](iamtimelinegroup-setsmartrecompressformat.md) перезаписывает частоту кадров.

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

 

 




