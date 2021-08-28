---
description: Начиная с TAPI 2,1, для управления и вывода диалоговых окон можно использовать библиотеки DLL пользовательского интерфейса поставщика услуг телефонии. TAPI загружает библиотеку DLL в процесс приложения, вызывающего любую из функций поставщика услуг, которые могут отображать диалоговое окно.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: Новые возможности для ТСПИ версии 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260978ad99bf49ed0beae0e71b2a02a794eef1a7af0c25074c20a08c1da054c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659824"
---
# <a name="whats-new-for-tspi-version-21"></a>Новые возможности для ТСПИ версии 2,1

Начиная с TAPI 2,1, для управления и вывода диалоговых окон можно использовать библиотеки DLL пользовательского интерфейса поставщика услуг телефонии. TAPI загружает библиотеку DLL в процесс приложения, вызывающего любую из функций поставщика услуг, которые могут отображать диалоговое окно.

Начиная с TAPI 2,1, можно реализовать обработчики запросов прокси-сервера. Обработчик — это полное приложение телефонии, которое обычно выполняется на сервере телефонии и предоставляет службы, которые более правильно реализуются в приложении, чем драйвер.

Функции и сообщения, которые были впервые или изменены для ТСПИ версии 2,1, следующие:

-   [**TSPI_lineConditionalMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   **TSPI_lineDropNoOwner**—**устарело**
-   **TSPI_lineDropOnClose**—**устарело**
-   [**TSPI_lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**TSPI_lineSetCallData**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**TSPI_lineSetCallQualityOfService**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**TSPI_lineSetCallTreatment**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [**TSPI_lineSetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**TSPI_phoneGetID**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [**TSPI_providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [**TSPI_providerShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   [**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))
-   [**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))
-   [**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))
-   [**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))
-   [**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))
-   [**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))
-   [**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))

Библиотека DLL пользовательского интерфейса поставщика услуг телефонии предоставляет возможность взаимодействия с пользователем в контексте приложения, а не самого поставщика услуг. ТСПИ версии 2,1 доставляет следующие новые функции, сообщения и структуры для реализации:

-   [**TSPI_providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [**TSPI_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [**TSPI_providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [**TUISPI_lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [**TUISPI_lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [**TUISPI_phoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [**TUISPI_providerConfig**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [**TUISPI_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [**TUISPI_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [**TUISPI_providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [**TUISPI_providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [**туиспикреатедиалогинстанцепарамс**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [**туиспидллкаллбакк**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [**LINE_CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
-   [**LINE_SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md)

 

 
