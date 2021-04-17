---
description: Метод Сркадд добавляет источник к дорожке.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'Метод Иамтимелинетракк:: Сркадд (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685228"
---
# <a name="iamtimelinetracksrcadd-method"></a>Метод Иамтимелинетракк:: Сркадд

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SrcAdd`Метод добавляет источник к дорожке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pSrc* 
</dt> <dd>

Указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) исходного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_При успешном выполнении возвращает значение ОК. Возвращает E \_ Interface, если объект не является исходным объектом. В противном случае возвращает значение **HRESULT** , указывающее причину ошибки.

## <a name="remarks"></a>Комментарии

Задайте время начала и окончания работы источника перед вызовом этого метода. (Вызовите [**иамтимелинеобж:: сетстартстоп**](iamtimelineobj-setstartstop.md).)

В настоящее время DES не может одновременно визуализировать более 75 источников, которые были сжаты с помощью кодеков для сжатия видео (ВКМ). Кроме того, если проект в целом содержит более 75 таких источников, необходимо использовать динамическое переподключение или DES не может выполнить предварительный просмотр проекта. Дополнительные сведения см. в разделе [**ирендеренгине:: сетдинамикреконнектлевел**](irenderengine-setdynamicreconnectlevel.md).

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

[**Интерфейс Иамтимелинетракк**](iamtimelinetrack.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




