---
description: Действие установки — это действие верхнего уровня, которое вызывается для установки или удаления компонентов.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Действие установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080624"
---
# <a name="install-action"></a><span data-ttu-id="0bd6b-103">Действие установки</span><span class="sxs-lookup"><span data-stu-id="0bd6b-103">INSTALL Action</span></span>

<span data-ttu-id="0bd6b-104">Действие установки — это действие верхнего уровня, которое вызывается для установки или удаления компонентов.</span><span class="sxs-lookup"><span data-stu-id="0bd6b-104">The INSTALL action is a top-level action called to install or remove components.</span></span> <span data-ttu-id="0bd6b-105">Это действие запрашивает [таблицу инсталлуисекуенце](installuisequence-table.md) и [таблицу инсталлексекутесекуенце](installexecutesequence-table.md) для выполнения действия, условия для выполнения действия и место действия в последовательности:</span><span class="sxs-lookup"><span data-stu-id="0bd6b-105">This action queries the [InstallUISequence Table](installuisequence-table.md) and [InstallExecuteSequence Table](installexecutesequence-table.md) for the action to execute, the condition for action execution, and the place of the action in the sequence:</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0bd6b-106">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="0bd6b-106">Sequence Restrictions</span></span>

<span data-ttu-id="0bd6b-107">Ограничения последовательности отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0bd6b-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0bd6b-108">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="0bd6b-108">ActionData Messages</span></span>

<span data-ttu-id="0bd6b-109">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="0bd6b-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd6b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bd6b-110">Remarks</span></span>

<span data-ttu-id="0bd6b-111">Действие установки не вызывается из последовательности таблицы действий, передается установщик Windows при вызове [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) или в исполняемом файле командной строки, Msiexec.exe вызывается с параметром командной строки "**/i**" или при вызове любой функции установщика, которая может выполнять задачу установки, например [**мсиконфигурефеатуре**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**мсипровидекомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)или [**мсиинсталлмиссингфиле**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="0bd6b-111">The INSTALL action is not called from within the action table sequence, it is passed to Windows Installer when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called, or the command line executable Msiexec.exe is called with the '**/i**' command line switch, or when any installer function is called that may perform an installation task, such as [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta), or [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span>

 

 



