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
ms.openlocfilehash: ee18eadbc535dd2cd4b48ec6f77adb1d3dec2f5a0c1f5065cee009e27635eda9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092304"
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



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**имедиарендерерактионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

