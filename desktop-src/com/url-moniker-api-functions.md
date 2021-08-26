---
title: Функции моникера URL-адреса
description: Функции моникера URL-адреса
ms.assetid: 773743d3-9434-4ec9-b85c-9b971e37682f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd4dc19d47a933e9f93516630b25fdab2f64b21cb3755ac9fd5bbdfa7edaba51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992044"
---
# <a name="url-moniker-functions"></a>Функции моникера URL-адреса

Функции моникера URL-адреса разделяют разработчиков от сложностей создания, управления и использования моникеров URL-адресов. Это следующие функции:

-   [**креатеурлмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85))
-   [**исвалидурл**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85))
-   [**регистермедиатипес**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))
-   [**креатеформатенумератор**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator)
-   [**регистерформатенумератор**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))
-   [**ревокеформатенумератор**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85))
-   [**регистермедиатипекласс**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))
-   [**финдмедиатипекласс**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))
-   [**жетклассфилеормиме**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))
-   [**урлмксетсессионоптион**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85))

Знакомство с этими функциями может быть следующим:

-   Ознакомьтесь с [**креатеурлмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85)) и [**исвалидурл**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85)) , если вы будете использовать моникеры URL-адресов в автономных приложениях. при разработке элемента управления ActiveX следует использовать [**ибиндхост:: креатемоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) вместо **креатеурлмоникер**.
-   Если вы будете выполнять согласование MIME с моникерами URL-адресов, вы должны быть знакомы с [**регистермедиатипес**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)), [**креатеформатенумератор**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator), [**регистерформатенумератор**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))и [**ревокеформатенумератор**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85)) .
-   Ознакомьтесь с [**регистермедиатипекласс**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85)), [**финдмедиатипекласс**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85)), [**жетклассфилеормиме**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))и [**урлмксетсессионоптион**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85)) только в том случае, если у вас есть существенная работа с моникерами URL-адресов и с COM.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Моникеры URL-адресов](url-monikers.md)
</dt> </dl>

 

 