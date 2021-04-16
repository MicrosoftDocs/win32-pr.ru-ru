---
title: Тестирование с помощью Аккчеккер
description: Описывает типичный рабочий процесс тестирования, включающий Аккчеккер.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- тестирование с помощью Аккчеккер
- Аккчеккер, Рабочий процесс тестирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531907"
---
# <a name="testing-with-accchecker"></a><span data-ttu-id="8dcb7-105">Тестирование с помощью Аккчеккер</span><span class="sxs-lookup"><span data-stu-id="8dcb7-105">Testing with AccChecker</span></span>

<span data-ttu-id="8dcb7-106">В следующем сценарии описаны действия, которые обычно выполняются при тестировании с помощью Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-106">The following scenario describes the steps that you typically follow when testing with AccChecker.</span></span>

> [!Note]  
> <span data-ttu-id="8dcb7-107">Когда выполняются подпрограммы проверки Аккчеккер, взаимодействие пользователей с ведущим компьютером может мешать некоторым подпрограммам.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-107">When AccChecker verification routines are running, user interaction with the host machine can interfere with some routines.</span></span> <span data-ttu-id="8dcb7-108">Рекомендуется не выполнять никаких действий пользователя, пока Аккчеккер не сообщит пользователю о том, что все задачи завершены.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-108">We recommend that no further user interaction occur until AccChecker notifies the user that all tasks are complete.</span></span>

 

1.  <span data-ttu-id="8dcb7-109">Выполните проверки Аккчеккер для определенного целевого приложения или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-109">Run AccChecker verifications on a particular target application or control.</span></span> <span data-ttu-id="8dcb7-110">Дополнительные сведения см. на [вкладке проверки](the-accchecker-graphical-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="8dcb7-110">For more information, see [Verifications Tab](the-accchecker-graphical-user-interface.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="8dcb7-111">Аккчеккер не исследует все перестановки пользовательского интерфейса в приложении.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-111">AccChecker doesn't explore all UI permutations in an application.</span></span> <span data-ttu-id="8dcb7-112">Элементы, скрытые в таких элементах управления, как окна, панели, вкладки и меню, должны предоставляться вручную.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-112">Elements hidden within controls such as windows, panes, tabs, and menus must be exposed manually.</span></span>

     

2.  <span data-ttu-id="8dcb7-113">Изучите журнал ошибок Аккчеккер и оцените или рассмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-113">Examine the AccChecker error log and assess or triage the results.</span></span> <span data-ttu-id="8dcb7-114">Устраните тривиальные проблемы и заносить серьезные ошибки в журнал соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-114">Fix trivial issues and log severe bugs as appropriate.</span></span>
3.  <span data-ttu-id="8dcb7-115">Создание файла подавления для ошибок и ошибок, которые можно пропустить до регрессионного тестирования.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-115">Generate a suppression file for bugs and errors that can be ignored until regression testing.</span></span>
4.  <span data-ttu-id="8dcb7-116">Повторно запустите проверки Аккчеккер с исправлением файла подавления и начальными ошибками.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-116">Re-run AccChecker verifications with the suppression file and initial bug fixes.</span></span> <span data-ttu-id="8dcb7-117">Это позволяет создать моментальный снимок проблем в текущей реализации Microsoft Active Accessibility и установить базовый план для регрессионного тестирования.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-117">This provides a snapshot of the issues in the current implementation of Microsoft Active Accessibility and establishes a baseline for regression testing.</span></span>
5.  <span data-ttu-id="8dcb7-118">Интегрируйте интерфейсы API Аккчеккер и файл подавления в среду автоматизированного тестирования для регрессионного тестирования на предмет ошибок, регистрируемых при первоначальной проверке Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-118">Integrate the AccChecker APIs and suppression file into an automated test framework for regression testing on bugs logged from the initial AccChecker verifications.</span></span>
    > [!Note]  
    > <span data-ttu-id="8dcb7-119">При исправлении ошибок файл подавления следует изменять по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-119">As bugs are fixed, the suppression file should be modified as required.</span></span>

     

6.  <span data-ttu-id="8dcb7-120">Убедитесь, что в приложение или элемент управления не появились регрессии или новые ошибки специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-120">Confirm that no regressions or new accessibility bugs have been introduced into the application or control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dcb7-121">См. также</span><span class="sxs-lookup"><span data-stu-id="8dcb7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dcb7-122">Средство UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="8dcb7-122">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




