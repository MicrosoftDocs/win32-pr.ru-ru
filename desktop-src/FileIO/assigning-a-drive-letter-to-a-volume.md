---
description: Вы можете назначить букву диска (например, X:) \) локальному тому с помощью функции сетволумемаунтпоинт, если для этой буквы диска уже не назначен том.
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Назначение буквы диска тому
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683193"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a><span data-ttu-id="b7232-103">Назначение буквы диска тому</span><span class="sxs-lookup"><span data-stu-id="b7232-103">Assigning a Drive Letter to a Volume</span></span>

<span data-ttu-id="b7232-104">Вы можете назначить букву диска (например, X:) \) локальному тому с помощью функции [**сетволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , если для этой буквы диска уже не назначен том.</span><span class="sxs-lookup"><span data-stu-id="b7232-104">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span> <span data-ttu-id="b7232-105">Если у локального тома уже есть буква диска,</span><span class="sxs-lookup"><span data-stu-id="b7232-105">If the local volume already has a drive letter.</span></span> <span data-ttu-id="b7232-106">затем [**сетволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b7232-106">then [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) will fail.</span></span> <span data-ttu-id="b7232-107">Чтобы справиться с этим, сначала удалите букву диска с помощью функции [**делетеволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="b7232-107">To handle this, first delete the drive letter by using the [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) function.</span></span> <span data-ttu-id="b7232-108">Пример кода см. в разделе [изменение назначения букв дисков](editing-drive-letter-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="b7232-108">For example code, see [Editing Drive Letter Assignments](editing-drive-letter-assignments.md).</span></span>

<span data-ttu-id="b7232-109">Система поддерживает не более одного буквы диска на том.</span><span class="sxs-lookup"><span data-stu-id="b7232-109">The system supports at most one drive letter per volume.</span></span> <span data-ttu-id="b7232-110">Таким образом, C: \\ и F: \\ представляют один и тот же том.</span><span class="sxs-lookup"><span data-stu-id="b7232-110">Therefore, you cannot have C:\\ and F:\\ represent the same volume.</span></span>

> [!Caution]
>
> <span data-ttu-id="b7232-111">Удаление существующей буквы диска и назначение новой может нарушить работу существующих путей, например, в ярлыках рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b7232-111">Deleting an existing drive letter and assigning a new one may break existing paths, such as those in desktop shortcuts.</span></span> <span data-ttu-id="b7232-112">Она также может привести к разрыву пути к программе, делающей букву диска.</span><span class="sxs-lookup"><span data-stu-id="b7232-112">It may also break the path to the program making the drive letter changes.</span></span> <span data-ttu-id="b7232-113">Благодаря управлению виртуальной памятью Windows это может привести к нарушению работы приложения, что приводит к нестабильному и неработоспособному состоянию системы.</span><span class="sxs-lookup"><span data-stu-id="b7232-113">With Windows virtual memory management, this may break the application, leaving the system in an unstable and possibly unusable state.</span></span> <span data-ttu-id="b7232-114">Разработчик программы обязан избегать таких потенциальных катастроф.</span><span class="sxs-lookup"><span data-stu-id="b7232-114">It is the program designer's responsibility to avoid such potential catastrophes.</span></span>

 

 

 



