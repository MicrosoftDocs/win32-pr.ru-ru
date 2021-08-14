---
title: Справочник по диспетчеру аудиосжатия
description: Справочник по диспетчеру аудиосжатия
ms.assetid: a4e234c7-4dd3-4269-90a5-5de2c8837c0f
keywords:
- Windows мультимедиа, справочник по ACM
- мультимедиа, Справочник по ACM
- мультимедиа аудио, Справочник по ACM
- аудио, Справочник по ACM)
- Диспетчер аудиосжатия (ACM), Справочник
- ACM (диспетчер аудиосжатия), справочные материалы
- Справочник по ACM, сведения
- Справочник по ACM, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29729fa19e67fb4695d8e6eca986488735d9b4529d9479615665a9ba2b5f3360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375801"
---
# <a name="audio-compression-manager-reference"></a>Справочник по диспетчеру аудиосжатия

В этом разделе описываются функции, структуры и сообщения, связанные с ACM. Эти элементы группируются следующим образом.

## <a name="drivers"></a>драйверы,

-   [**акмдриверадд**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**акмдриверклосе**](/windows/desktop/api/Msacm/nf-msacm-acmdriverclose)
-   [**акмдривердетаилс**](/windows/win32/api/msacm/ns-msacm-acmdriverdetails)
-   [**акмдриверенум**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum)
-   [**акмдриверенумкаллбакк**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**акмдриверид**](/windows/desktop/api/Msacm/nf-msacm-acmdriverid)
-   [**акмдривермессаже**](/windows/desktop/api/Msacm/nf-msacm-acmdrivermessage)
-   [**акмдриверопен**](/windows/desktop/api/Msacm/nf-msacm-acmdriveropen)
-   [**акмдриверприорити**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**акмдриверпрок**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)
-   [**акмдриверремове**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

## <a name="filters"></a>Фильтры

-   [**акмфилтерчусе**](/windows/win32/api/msacm/ns-msacm-acmfilterchoose)
-   [**акмфилтерчусехукпрок**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**акмфилтердетаилс**](/windows/win32/api/msacm/ns-msacm-acmfilterdetails)
-   [**акмфилтеренум**](/windows/desktop/api/Msacm/nf-msacm-acmfilterenum)
-   [**акмфилтеренумкаллбакк**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**акмфилтертагдетаилс**](/windows/win32/api/msacm/ns-msacm-acmfiltertagdetails)
-   [**акмфилтертаженум**](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagenum)
-   [**акмфилтертаженумкаллбакк**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)

## <a name="formats"></a>Форматы

-   [**акмформатчусе**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)
-   [**акмформатчусехукпрок**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)
-   [**акмформатдетаилс**](/windows/win32/api/msacm/ns-msacm-acmformatdetails)
-   [**акмформатенум**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum)
-   [**акмформатенумкаллбакк**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**акмформатсугжест**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest)
-   [**акмформаттагдетаилс**](/windows/win32/api/msacm/ns-msacm-acmformattagdetails)
-   [**акмформаттаженум**](/windows/desktop/api/Msacm/nf-msacm-acmformattagenum)
-   [**акмформаттаженумкаллбакк**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)

## <a name="messages"></a>Сообщения

-   [**MM \_ ACM \_ филтерчусе**](mm-acm-filterchoose.md)
-   [**MM \_ ACM \_ форматчусе**](mm-acm-formatchoose.md)

## <a name="streams"></a>Потоки

-   [**акмстреамклосе**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)
-   [**акмстреамконверт**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)
-   [**акмстреамконверткаллбакк**](/previous-versions//dd742925(v=vs.85))
-   [**акмстреамхеадер**](/windows/win32/api/msacm/ns-msacm-acmstreamheader)
-   [**акмстреаммессаже**](/windows/desktop/api/Msacm/nf-msacm-acmstreammessage)
-   [**акмстреамопен**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)
-   [**акмстреампрепарехеадер**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)
-   [**акмстреамресет**](/windows/desktop/api/Msacm/nf-msacm-acmstreamreset)
-   [**акмстреамсизе**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)
-   [**акмстреамунпрепарехеадер**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)

## <a name="miscellaneous"></a>Разное

-   [**акмжетверсион**](/windows/desktop/api/Msacm/nf-msacm-acmgetversion)
-   [**акмметрикс**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Диспетчер аудиосжатия](audio-compression-manager.md)
</dt> </dl>

 

 