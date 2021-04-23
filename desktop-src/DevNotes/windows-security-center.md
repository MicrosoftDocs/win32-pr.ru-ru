---
description: Центр обеспечения безопасности Windows
ms.assetid: FF0D7B81-AFDC-4DB2-B2B0-0D2536B2757B
title: Центр обеспечения безопасности Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694185b0a0fed7af9c2ab3d7965674c02354c079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140891"
---
# <a name="windows-security-center"></a><span data-ttu-id="d57ea-103">Центр обеспечения безопасности Windows</span><span class="sxs-lookup"><span data-stu-id="d57ea-103">Windows Security Center</span></span>

<span data-ttu-id="d57ea-104">Центр безопасности Windows (WSC) — это комплексное средство создания отчетов, помогающее пользователям устанавливать и обслуживать защитные уровни безопасности на компьютерах.</span><span class="sxs-lookup"><span data-stu-id="d57ea-104">Windows Security Center (WSC) is a comprehensive reporting tool that helps users establish and maintain a protective security layer around their computer systems.</span></span> <span data-ttu-id="d57ea-105">После установки уровня безопасности центр безопасности Windows инконспикуаусся, так как он отслеживает состояние работоспособности компьютера.</span><span class="sxs-lookup"><span data-stu-id="d57ea-105">Once a security layer is established, Windows Security Center is inconspicuous as it monitors the computer’s health state.</span></span> <span data-ttu-id="d57ea-106">Однако если существуют уязвимости, WSC предоставляет предупреждения и рекомендации, помогающие пользователю добиться безопасного состояния, которое будет выводится для пользователя в центре поддержки.</span><span class="sxs-lookup"><span data-stu-id="d57ea-106">However, if vulnerabilities exist, WSC provides alerts and prescriptive guidance to assist the user in achieving a secure state which is surfaced to the end user through the Action Center.</span></span>

<span data-ttu-id="d57ea-107">Чтобы решения безопасности сторонних производителей (антивирусные программы, Антивредоносные программы или антишпионские программы) были совместимы с Windows и успешно отправляют состояние в центр поддержки, им необходимо зарегистрироваться в центре безопасности и сообщить о каждом последующем изменении состояния с помощью частных API для взаимодействия с WSC.</span><span class="sxs-lookup"><span data-stu-id="d57ea-107">In order for third party security solutions (antivirus, antimalware, or antispyware) to be compliant with Windows and successfully report status to Action Center, they are required to register themselves with Security Center and report any subsequent status changes using private APIs for communicating with WSC.</span></span> <span data-ttu-id="d57ea-108">WSC, в свою очередь, передает эти обновления в центр поддержки, где они в конечном итоге отображаются конечному пользователю.</span><span class="sxs-lookup"><span data-stu-id="d57ea-108">WSC, in turn, communicates these updates to Action Center, where they are finally displayed to the end user.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d57ea-109">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="d57ea-109">In this section</span></span>

-   [<span data-ttu-id="d57ea-110">Перечисления центра безопасности Windows</span><span class="sxs-lookup"><span data-stu-id="d57ea-110">Windows Security Center Enumerations</span></span>](windows-security-center-enumerations.md)
-   [<span data-ttu-id="d57ea-111">Интерфейсы центра безопасности Windows</span><span class="sxs-lookup"><span data-stu-id="d57ea-111">Windows Security Center Interfaces</span></span>](windows-security-center-interfaces.md)
-   [<span data-ttu-id="d57ea-112">Функции центра безопасности Windows</span><span class="sxs-lookup"><span data-stu-id="d57ea-112">Windows Security Center Functions</span></span>](windows-security-center-functions.md)

 

 



