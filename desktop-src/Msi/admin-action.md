---
description: Действие администратора — это действие верхнего уровня, используемое для выполнения административных установок.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Действие администратора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909127"
---
# <a name="admin-action"></a><span data-ttu-id="9859c-103">Действие администратора</span><span class="sxs-lookup"><span data-stu-id="9859c-103">ADMIN Action</span></span>

<span data-ttu-id="9859c-104">Действие администратора — это действие верхнего уровня, используемое для выполнения [административных установок](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="9859c-104">The ADMIN action is a top-level action used to perform [administrative installations](administrative-installation.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9859c-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="9859c-105">Sequence Restrictions</span></span>

<span data-ttu-id="9859c-106">Ограничения последовательности отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="9859c-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9859c-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="9859c-107">ActionData Messages</span></span>

<span data-ttu-id="9859c-108">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="9859c-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="9859c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9859c-109">Remarks</span></span>

<span data-ttu-id="9859c-110">Действие администратора не вызывается из последовательности таблицы действий, установщик Windows выполняет это действие при вызове [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) с параметром *сзкоммандлине* , для которого задано значение Action = Admin, или исполняемый файл командной строки, Msiexec.exe вызывается с параметром командной строки "/a".</span><span class="sxs-lookup"><span data-stu-id="9859c-110">The ADMIN action is not called from within the action table sequence, Windows Installer executes this action when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to "ACTION=ADMIN" or the command line executable Msiexec.exe is called with the '/a' command line switch.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9859c-111">См. также</span><span class="sxs-lookup"><span data-stu-id="9859c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9859c-112">Таблица Админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="9859c-112">AdminUISequence Table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="9859c-113">Таблица Админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="9859c-113">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)
</dt> </dl>

 

 



