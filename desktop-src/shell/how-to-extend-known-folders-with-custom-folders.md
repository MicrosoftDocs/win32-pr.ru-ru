---
description: Независимые поставщики программного обеспечения могут расширять набор известных папок в системе путем регистрации собственных папок.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Расширение известных папок с помощью пользовательских папок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264421"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a><span data-ttu-id="d3a9c-103">Расширение известных папок с помощью пользовательских папок</span><span class="sxs-lookup"><span data-stu-id="d3a9c-103">How to Extend Known Folders with Custom Folders</span></span>

<span data-ttu-id="d3a9c-104">Независимые поставщики программного обеспечения могут расширять набор известных папок в системе путем регистрации собственных папок.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-104">Independent software vendors (ISVs) can extend the set of known folders on a system by registering known folders of their own.</span></span> <span data-ttu-id="d3a9c-105">После регистрации эти сторонние папки известны системе.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-105">Once registered, those third-party folders are known to the system.</span></span> <span data-ttu-id="d3a9c-106">Они обнаруживаются любым вызовом [**икновнфолдерманажер:: жетфолдеридс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span><span class="sxs-lookup"><span data-stu-id="d3a9c-106">They are found by any call to [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span></span> <span data-ttu-id="d3a9c-107">Обратите внимание, что известная папка должна быть папкой на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-107">Note that a known folder must be a per-machine folder.</span></span> <span data-ttu-id="d3a9c-108">Нельзя создать известную папку для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-108">You cannot create a per-user known folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="d3a9c-109">Инструкции</span><span class="sxs-lookup"><span data-stu-id="d3a9c-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="d3a9c-110">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-110">Step 1:</span></span>

<span data-ttu-id="d3a9c-111">Определите свою известную папку с помощью структуры [**\_ определения кновнфолдер**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) .</span><span class="sxs-lookup"><span data-stu-id="d3a9c-111">Define your known folder through a [**KNOWNFOLDER\_DEFINITION**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) structure.</span></span>

### <a name="step-2"></a><span data-ttu-id="d3a9c-112">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-112">Step 2:</span></span>

<span data-ttu-id="d3a9c-113">Зарегистрируйте известную папку с помощью вызова [**икновнфолдерманажер:: регистерфолдер**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span><span class="sxs-lookup"><span data-stu-id="d3a9c-113">Register the known folder through a call to [**IKnownFolderManager::RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3a9c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3a9c-114">Remarks</span></span>

<span data-ttu-id="d3a9c-115">При создании известной папки для приложения в рамках процедуры установки необходимо также включить [**икновнфолдерманажер:: унрегистерфолдер**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) в составе кода удаления.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-115">If you create a known folder for your application as part of your installation procedure, you must also include [**IKnownFolderManager::UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) as part of your uninstallation code.</span></span>

<span data-ttu-id="d3a9c-116">Обратите внимание на необходимость включения папки в известную систему папок перед ее регистрацией.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-116">Give consideration to why you want your folder to be included in the known folder system before you register it.</span></span> <span data-ttu-id="d3a9c-117">У вас должна быть допустимая причина повышения прав доступа к папке до такого уровня видимости системы.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-117">You should have a valid reason for elevating your folder to that level of system visibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3a9c-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d3a9c-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d3a9c-119">[Пример: известные папки](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3a9c-119">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
