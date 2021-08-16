---
description: Метод Сетбуфферсамплес указывает, следует ли копировать демонстрационные данные в буфер, так как он проходит через фильтр.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'Метод Исамплеграббер:: Сетбуфферсамплес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c768a21d4e08e6900f3a46f3e398f5040aaf6b6b0bc45c9187ac07821500a372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817999"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>Метод Исамплеграббер:: Сетбуфферсамплес

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Метод **сетбуфферсамплес** указывает, следует ли копировать демонстрационные данные в буфер, так как он проходит через фильтр.

## <a name="syntax"></a>Синтаксис


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*буфферсем* 
</dt> <dd>

Логическое значение, указывающее, следует ли заменять образец данных в буфер. Если **значение — true**, фильтр копирует демонстрационные данные во внутренний буфер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Чтобы получить скопированный буфер, вызовите метод [**исамплеграббер:: жеткуррентбуффер**](isamplegrabber-getcurrentbuffer.md).

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование образца захвата](using-the-sample-grabber.md)
</dt> <dt>

[**Интерфейс Исамплеграббер**](isamplegrabber.md)
</dt> </dl>

 

 




