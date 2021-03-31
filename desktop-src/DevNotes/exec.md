---
description: HKLM \\ программное обеспечение \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807720"
---
# <a name="exec"></a><span data-ttu-id="7bdc1-103">Exec</span><span class="sxs-lookup"><span data-stu-id="7bdc1-103">Exec</span></span>

<span data-ttu-id="7bdc1-104">**HKLM \\ программное обеспечение \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**</span><span class="sxs-lookup"><span data-stu-id="7bdc1-104">**HKLM\\Software\\Microsoft\\Internet Explorer\\Extensions\\{e2e2dd38-d088-4134-82b7-f2ba38496583}**</span></span>



| <span data-ttu-id="7bdc1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7bdc1-105">Data type</span></span> | <span data-ttu-id="7bdc1-106">Диапазон</span><span class="sxs-lookup"><span data-stu-id="7bdc1-106">Range</span></span>                    | <span data-ttu-id="7bdc1-107">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7bdc1-107">Default value</span></span> |
|-----------|--------------------------|---------------|
| <span data-ttu-id="7bdc1-108">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7bdc1-108">REG\_SZ</span></span>   | <span data-ttu-id="7bdc1-109">*Путь к исполняемому файлу*</span><span class="sxs-lookup"><span data-stu-id="7bdc1-109">*Path to the executable*</span></span> |               |



 

## <a name="browser-integration-steps"></a><span data-ttu-id="7bdc1-110">Шаги интеграции с браузером</span><span class="sxs-lookup"><span data-stu-id="7bdc1-110">Browser Integration Steps</span></span>

1.  <span data-ttu-id="7bdc1-111">Используйте функцию [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) , чтобы определить, установлена ли диагностика сети.</span><span class="sxs-lookup"><span data-stu-id="7bdc1-111">Use the [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) function to determine whether the Network Diagnostic is installed.</span></span> <span data-ttu-id="7bdc1-112">Если он установлен, будет указан ключ **{e2e2dd38-d088-4134-82b7-f2ba38496583}** .</span><span class="sxs-lookup"><span data-stu-id="7bdc1-112">If it is installed, the **{e2e2dd38-d088-4134-82b7-f2ba38496583}** key is present.</span></span>
2.  <span data-ttu-id="7bdc1-113">Используйте функцию [**процедура RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) , чтобы получить путь к исполняемому файлу диагностики сети из записи **exec** .</span><span class="sxs-lookup"><span data-stu-id="7bdc1-113">Use the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to retrieve the path of the Network Diagnostic executable file from the **Exec** entry.</span></span>
3.  <span data-ttu-id="7bdc1-114">Отобразить новую страницу ошибки, если она установлена в системе.</span><span class="sxs-lookup"><span data-stu-id="7bdc1-114">Display the new error page if the diagnostic is installed on the system.</span></span>
4.  <span data-ttu-id="7bdc1-115">Создайте расширение браузера, которое создает стандартный элемент панели инструментов, если в системе установлен модуль диагностики.</span><span class="sxs-lookup"><span data-stu-id="7bdc1-115">Create a browser extension that creates a standard toolbar item if the diagnostic is installed on the system.</span></span>
5.  <span data-ttu-id="7bdc1-116">Запустите исполняемый файл диагностики сети, используя путь, полученный на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="7bdc1-116">Execute the Network Diagnostic executable using the path retrieved in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bdc1-117">См. также</span><span class="sxs-lookup"><span data-stu-id="7bdc1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bdc1-118">Обзор функций средств диагностики сети</span><span class="sxs-lookup"><span data-stu-id="7bdc1-118">Network Diagnostics Tools Feature Overview</span></span>](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
