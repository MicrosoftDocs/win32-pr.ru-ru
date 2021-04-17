---
description: 'Интерфейс Исамплеграбберкб предоставляет методы обратного вызова для метода Исамплеграббер:: Сеткаллбакк. Если приложение вызывает этот метод, он должен реализовать этот интерфейс. Дополнительные сведения см. в разделе Исамплеграббер.'
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Интерфейс Исамплеграбберкб (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675177"
---
# <a name="isamplegrabbercb-interface"></a>Интерфейс Исамплеграбберкб

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`ISampleGrabberCB`Интерфейс предоставляет методы обратного вызова для метода [**исамплеграббер:: сеткаллбакк**](isamplegrabber-setcallback.md) . Если приложение вызывает этот метод, он должен реализовать этот интерфейс. Дополнительные сведения см. в разделе [**исамплеграббер**](isamplegrabber.md).

## <a name="members"></a>Элементы

Интерфейс **исамплеграбберкб** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Исамплеграбберкб** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **исамплеграбберкб** содержит следующие методы.



| Метод                                        | Описание                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**буфферкб**](isamplegrabbercb-buffercb.md) | Метод обратного вызова, который получает указатель на образец буфера.<br/> |
| [**самплекб**](isamplegrabbercb-samplecb.md) | Метод обратного вызова, который получает указатель на пример носителя.<br/>  |



 

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



 

 
