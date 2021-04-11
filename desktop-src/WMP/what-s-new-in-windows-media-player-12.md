---
title: Что нового в проигрывателе Windows Media 12
description: В этом разделе перечислены новые возможности проигрывателя Windows Media 12.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Проигрыватель Windows Media, новые возможности
- Проигрыватель Windows Media, новые функции
- пакет средств разработки программного обеспечения (SDK), проигрыватель Windows Media 12
- Пакет SDK (пакет средств разработки программного обеспечения), проигрыватель Windows Media 12
- Документация, Windows Media Player 12 SDK
- новые возможности, проигрыватель Windows Media 12
- новые возможности, проигрыватель Windows Media 12
- интерфейсы, новые возможности проигрывателя Windows Media 12
- атрибуты, новые функции в проигрывателе Windows Media 12
- метаданные, новые функции в проигрывателе Windows Media 12
- перечисления, новые функции в проигрывателе Windows Media 12
- Флаги, новые функции в проигрывателе Windows Media 12
- интерфейсы, устаревшие в проигрывателе Windows Media 12
- методы, устаревшие в проигрывателе Windows Media 11 и не 12
- версии проигрывателя Windows Media, новые функции в версии 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104133606"
---
# <a name="whats-new-in-windows-media-player-12"></a>Что нового в проигрывателе Windows Media 12

В этом разделе перечислены новые возможности проигрывателя Windows Media 12.

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

Следующие методы были устаревшими в пакете SDK для проигрывателя Windows Media 11, но больше не являются устаревшими.

-   [**Ивмпграфкреатион:: Графкреатионпререндер**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [**Ивмпграфкреатион:: Графкреатионпострендер**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сведения о пакете SDK проигрывателя Windows Media](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




