---
title: Имедиарендерерактионинформатион Иссетнекстсаурцеаваилабле, метод
description: Извлекает значение, указывающее, принимает ли ДМР в настоящее время метод Сетнекстсаурцефромуриасинк, метод Сетнекстсаурцефромстреамасинк или метод Сетнекстсаурцефроммедиасаурцеасинк.
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- API потоковой передачи мультимедиа метода Иссетнекстсаурцеаваилабле
- API потоковой передачи мультимедиа метода Иссетнекстсаурцеаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Иссетнекстсаурцеаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 265a9a96d5229e47008c60813fd6c0e3bc567800
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790567"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a>Метод Имедиарендерерактионинформатион:: Иссетнекстсаурцеаваилабле

Извлекает значение, указывающее, принимает ли ДМР в настоящее время метод [**сетнекстсаурцефромуриасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , метод [**Сетнекстсаурцефромстреамасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) или метод [**сетнекстсаурцефроммедиасаурцеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Логическое значение, равное **true** , если ДМР в настоящее время принимает метод [**Сетнекстсаурцефромуриасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , метод [**Сетнекстсаурцефромстреамасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) или метод [**сетнекстсаурцефроммедиасаурцеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) и **значение false** в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имедиарендерерактионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

