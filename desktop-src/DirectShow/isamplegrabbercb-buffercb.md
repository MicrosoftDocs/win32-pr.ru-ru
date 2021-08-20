---
description: Метод Буфферкб — это метод обратного вызова, который получает указатель на образец буфера.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'Метод Исамплеграбберкб:: Буфферкб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c92e83c8daf5bf129a9aa8330bcc53caa88537f2395aeceebd8b5da2037c5b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817594"
---
# <a name="isamplegrabbercbbuffercb-method"></a>Метод Исамплеграбберкб:: Буфферкб

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Метод **буфферкб** — это метод обратного вызова, который получает указатель на образец буфера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*самплетиме* 
</dt> <dd>

Время начала выборки в секундах.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Указатель на буфер, содержащий образец данных. Формат данных зависит от типа носителя входного ПИН-кода захвата выборки. Чтобы получить тип мультимедиа, вызовите [**исамплеграббер:: жетконнектедмедиатипе**](isamplegrabber-getconnectedmediatype.md).

</dd> <dt>

*буфферлен* 
</dt> <dd>

Длина буфера, на который указывает *pBuffer*, в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение \_ ОК в случае успеха или код ошибки **HRESULT** в противном случае.

## <a name="remarks"></a>Remarks

Этот метод обратного вызова получает указатель на данные в последнем примере носителя.

> [!Note]  
> Этот метод получает указатель на исходный образец данных, а не копию. Исходная документация неправильно объявила, что *pBuffer* содержит копию данных.

 

Чтобы настроить обратный вызов, вызовите [**исамплеграббер:: сеткаллбакк**](isamplegrabber-setcallback.md).

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

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> <dt>

[**Интерфейс Исамплеграбберкб**](isamplegrabbercb.md)
</dt> </dl>

 

 




