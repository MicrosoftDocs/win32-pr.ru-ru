---
title: Что нового в проигрывателе Windows Media 12
description: в этом разделе перечислены новые возможности проигрыватель Windows Media 12.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- проигрыватель Windows Media, новые возможности
- проигрыватель Windows Media, новые функции
- пакет средств разработки программного обеспечения (SDK), проигрыватель Windows Media 12
- пакет SDK (пакет средств разработки программного обеспечения), проигрыватель Windows Media 12
- документация, пакет SDK для проигрыватель Windows Media 12
- новые возможности, проигрыватель Windows Media 12
- новые функции, проигрыватель Windows Media 12
- интерфейсы, новые функции в проигрыватель Windows Media 12
- атрибуты, новые функции в проигрыватель Windows Media 12
- метаданные, новые функции в проигрыватель Windows Media 12
- перечисления, новые функции в проигрыватель Windows Media 12
- флаги, новые функции в проигрыватель Windows Media 12
- интерфейсы, устаревшие в проигрыватель Windows Media 12
- методы, устаревшие в проигрыватель Windows Media 11 и не 12
- версии проигрыватель Windows Media, новые функции в версии 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 976c9b0995188f9d6c6db6e7394ec0019047ff18b51940ada202c8c7ea713f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862284"
---
# <a name="whats-new-in-windows-media-player-12"></a>Что нового в проигрывателе Windows Media 12

в этом разделе перечислены новые возможности проигрыватель Windows Media 12.

## <a name="new-interfaces"></a>Новые интерфейсы

-   [**ивмпаудиорендерконфиг**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a>Новые атрибуты

Следующие новые атрибуты для элементов мультимедиа доступны через интерфейсы [**ивмпмедиа**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) и [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) .

-   [**албумковерурл**](wm-albumcoverurl-attribute.md)
-   [**алтернатесаурцеурл**](alternatesourceurl-attribute.md)
-   [**длнасаурцеури**](dlnasourceuri-attribute.md)
-   [**длнасерверудн**](dlnaserverudn-attribute.md)
-   [**дткпифост**](dtcpiphost-attribute.md)
-   [**дткпиппорт**](dtcpipport-attribute.md)
-   [**либрарид**](libraryid-attribute.md)
-   [**LibraryName**](libraryname-attribute.md)

## <a name="new-device-metadata"></a>Новые метаданные устройства

Следующие новые элементы метаданных устройства можно получить путем вызова [**ивмпсинкдевице:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).

-   **баккграундсинкстате**
-   **скиппедфилес**
-   **синкфилтер**

Следующие новые элементы метаданных устройства можно задать путем вызова [**IWMPSyncDevice2:: сетитеминфо**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).

-   **аутосинкдефаултрулес**
-   **баккграундсинкстате**
-   **инклудескиппедфилес**
-   **синкфилтер**
-   **синконконнект**

## <a name="new-enumeration-member"></a>Новый член перечисления

Перечисление [**вмпсинкстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) имеет следующий новый элемент.

-   **вмпссестиматинг**

## <a name="new-flag"></a>Новый флаг

Метод [**ивмпграфкреатион:: жетграфкреатионфлагс**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) поддерживает следующий новый флаг.

-   **\_Флаги вмпгк \_ использовать \_ настраиваемый \_ граф**

## <a name="deprecated-interface"></a>Устаревший интерфейс

Следующий интерфейс является устаревшим.

-   [**ивмпфолдермониторсервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a>Методы, которые больше не являются устаревшими

следующие методы были устаревшими в пакете SDK для проигрыватель Windows Media 11, но больше не являются устаревшими.

-   [**Ивмпграфкреатион:: Графкреатионпререндер**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [**Ивмпграфкреатион:: Графкреатионпострендер**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[сведения о пакете SDK для проигрыватель Windows Media](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




