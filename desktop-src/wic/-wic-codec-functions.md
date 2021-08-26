---
title: Функции WIC
description: в этом разделе содержатся сведения о функциях компонента обработки изображений Windows (WIC).
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f60660780e97831a77101c15646385d62048f005279b388a532ca687a200996
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056804"
---
# <a name="wic-functions"></a>Функции WIC

в этом разделе содержатся сведения о функциях компонента обработки изображений Windows (WIC).

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                      | Описание                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*прогресснотификатионкаллбакк*](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | Определенная приложением функция обратного вызова, вызываемая при выполнении компонента кодека.<br/>                                                                                                                        |
| [**викконвертбитмапсаурце**](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | Получает [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) в нужном формате пикселей из заданного **IWICBitmapSource**.<br/>                                                                           |
| [**виккреатебитмапфромсектион**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | возвращает [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , который поддерживается пикселами обработчика раздела Windows интерфейс графических устройств (GDI).<br/>                                                |
| [**виккреатебитмапфромсектионекс**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | Возвращает [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , который поддерживается пикселами в маркере раздела GDI.<br/>                                                                                    |
| [**викжетметадатаконтентсизе**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | Возвращает размер содержимого метаданных, содержащегося в указанном [**ивикметадатавритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter). Возвращенный размер учетных записей для заголовка и длины метаданных.<br/> |
| [**викмапгуидтошортнаме**](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | Получает короткое имя, связанное с данным идентификатором GUID.<br/>                                                                                                                                                       |
| [**викмапсчематонаме**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | Получает имя, связанное с заданной схемой.<br/>                                                                                                                                                           |
| [**викмапшортнаметогуид**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | Получает идентификатор GUID, связанный с заданным коротким именем.<br/>                                                                                                                                                     |
| [**викматчметадатаконтент**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | Получает GUID формата метаданных для указанного формата контейнера и поставщика, который наилучшим образом соответствует содержимому в данном потоке.<br/>                                                                            |
| [**виксериализеметадатаконтент**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | Записывает метаданные в заданный поток.<br/>                                                                                                                                                                       |
| [Функции прокси-сервера WIC](wic-proxy-functions.md)<br/>                                  | Этот раздел содержит функции прокси-сервера WIC.<br/>                                                                                                                                                             |



 

 

 




