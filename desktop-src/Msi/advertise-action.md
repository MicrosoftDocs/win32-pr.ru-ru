---
description: Действие объявления — это действие верхнего уровня, которое вызывается для установки или удаления объявленных компонентов.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Действие объявления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813352"
---
# <a name="advertise-action"></a><span data-ttu-id="97379-103">Действие объявления</span><span class="sxs-lookup"><span data-stu-id="97379-103">ADVERTISE Action</span></span>

<span data-ttu-id="97379-104">Действие объявления — это действие верхнего уровня, которое вызывается для установки или удаления объявленных компонентов.</span><span class="sxs-lookup"><span data-stu-id="97379-104">The ADVERTISE action is a top-level action called to install or remove advertised components.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="97379-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="97379-105">Sequence Restrictions</span></span>

<span data-ttu-id="97379-106">Ограничения последовательности отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="97379-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="97379-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="97379-107">ActionData Messages</span></span>

<span data-ttu-id="97379-108">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="97379-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="97379-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97379-109">Remarks</span></span>

<span data-ttu-id="97379-110">[*Объявление*](a-gly.md) относится к возможности установщика по обеспечению загрузки и запуска интерфейсов приложения без физической установки приложения.</span><span class="sxs-lookup"><span data-stu-id="97379-110">[*Advertising*](a-gly.md) refers to the installer's ability to provide the loading and launching interfaces of an application without physically installing the application.</span></span> <span data-ttu-id="97379-111">Установщик не устанавливает необходимые компоненты до тех пор, пока пользователь или приложение не активируют объявленный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="97379-111">The installer does not install the necessary components until a user or application activates an advertised interface.</span></span> <span data-ttu-id="97379-112">Эта концепция называется [*Install-On-Demand*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="97379-112">This concept is called [*install-on-demand*](i-gly.md).</span></span>

<span data-ttu-id="97379-113">Действие объявления не вызывается из последовательности таблицы действий, установщик Windows выполняет это действие, когда исполняемый файл командной строки Msiexec.exe вызывается с параметром командной строки "/j" или когда вызывается [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) с параметром *сзкоммандлине* , для которого задано действие = объявление.</span><span class="sxs-lookup"><span data-stu-id="97379-113">The ADVERTISE action is not called from within the action table sequence, the Windows Installer executes this action when the command line executable Msiexec.exe is called with the '/j' command line switch or when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to ACTION=ADVERTISE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97379-114">См. также</span><span class="sxs-lookup"><span data-stu-id="97379-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97379-115">Таблица Адвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="97379-115">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)
</dt> </dl>

 

 



