---
description: ICE64 проверяет правильность удаления новых каталогов в профиле пользователя в сценариях роуминга.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546138"
---
# <a name="ice64"></a><span data-ttu-id="f0ba7-103">ICE64</span><span class="sxs-lookup"><span data-stu-id="f0ba7-103">ICE64</span></span>

<span data-ttu-id="f0ba7-104">ICE64 проверяет правильность удаления новых каталогов в профиле пользователя в сценариях роуминга.</span><span class="sxs-lookup"><span data-stu-id="f0ba7-104">ICE64 checks that new directories in the user profile are removed correctly in roaming scenarios.</span></span>

<span data-ttu-id="f0ba7-105">Ошибка при исправлении предупреждения или ошибки, о которой сообщает ICE64, обычно приводит к проблемам при полной очистке компьютера во время удаления.</span><span class="sxs-lookup"><span data-stu-id="f0ba7-105">Failure to fix a warning or error reported by ICE64 generally leads to problems in completely cleaning the computer during an uninstallation.</span></span> <span data-ttu-id="f0ba7-106">Когда перемещаемый пользователь, установивший приложение, входит в систему на компьютере в первый раз, весь профиль копируется на компьютер.</span><span class="sxs-lookup"><span data-stu-id="f0ba7-106">When a roaming user who has installed the application logs on to a computer for the first time, all of the profile is copied down onto the computer.</span></span> <span data-ttu-id="f0ba7-107">В объявлении (которое происходит после загрузки перемещаемого профиля) установщик проверяет, что каталог уже существует и, следовательно, не удаляет его при удалении.</span><span class="sxs-lookup"><span data-stu-id="f0ba7-107">On advertisement (which takes place after the roaming profile download), the Installer verifies that the directory is already there and therefore does not delete it on uninstallation.</span></span> <span data-ttu-id="f0ba7-108">Это оставляет каталог на компьютере пользователя безвозвратно.</span><span class="sxs-lookup"><span data-stu-id="f0ba7-108">This leaves the directory on the user's computer permanently.</span></span>

## <a name="result"></a><span data-ttu-id="f0ba7-109">Результат</span><span class="sxs-lookup"><span data-stu-id="f0ba7-109">Result</span></span>

<span data-ttu-id="f0ba7-110">ICE64 отправляет предупреждение или ошибку в случае роуминга, если новый каталог в профиле пользователя, который необходимо удалить, не удаляется.</span><span class="sxs-lookup"><span data-stu-id="f0ba7-110">ICE64 posts a warning or an error in a roaming situation if a new directory in the user profile that should be removed is not removed.</span></span>

## <a name="example"></a><span data-ttu-id="f0ba7-111">Пример</span><span class="sxs-lookup"><span data-stu-id="f0ba7-111">Example</span></span>

<span data-ttu-id="f0ba7-112">ICE64 сообщает об ошибке в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="f0ba7-112">ICE64 reports the following error for the example shown.</span></span>

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

<span data-ttu-id="f0ba7-113">Папка "Мйосерфолдер" является пользовательской папкой профиля.</span><span class="sxs-lookup"><span data-stu-id="f0ba7-113">The folder 'MyOtherFolder' is a custom profile folder.</span></span> <span data-ttu-id="f0ba7-114">Так как он не указан в таблице Ремовефиле, он не удаляется в некоторых сценариях.</span><span class="sxs-lookup"><span data-stu-id="f0ba7-114">Because it is not listed in the RemoveFile table, it is not removed in some scenarios.</span></span>

<span data-ttu-id="f0ba7-115">Чтобы устранить эту ошибку, создайте строку для папки в таблице Ремовефиле.</span><span class="sxs-lookup"><span data-stu-id="f0ba7-115">To fix this error, create a row for the folder in the RemoveFile table.</span></span>

[<span data-ttu-id="f0ba7-116">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="f0ba7-116">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="f0ba7-117">Каталог</span><span class="sxs-lookup"><span data-stu-id="f0ba7-117">Directory</span></span>     | <span data-ttu-id="f0ba7-118">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="f0ba7-118">Directory\_Parent</span></span> | <span data-ttu-id="f0ba7-119">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="f0ba7-119">DefaultDir</span></span>  |
|---------------|-------------------|-------------|
| <span data-ttu-id="f0ba7-120">аппдатафолдер</span><span class="sxs-lookup"><span data-stu-id="f0ba7-120">AppDataFolder</span></span> | <span data-ttu-id="f0ba7-121">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="f0ba7-121">TARGETDIR</span></span>         |             |
| <span data-ttu-id="f0ba7-122">MyFolder</span><span class="sxs-lookup"><span data-stu-id="f0ba7-122">MyFolder</span></span>      | <span data-ttu-id="f0ba7-123">аппдатафолдер</span><span class="sxs-lookup"><span data-stu-id="f0ba7-123">AppDataFolder</span></span>     | <span data-ttu-id="f0ba7-124">Папка с подкаталогами</span><span class="sxs-lookup"><span data-stu-id="f0ba7-124">DataFolder</span></span>  |
| <span data-ttu-id="f0ba7-125">мйосерфолдер</span><span class="sxs-lookup"><span data-stu-id="f0ba7-125">MyOtherFolder</span></span> | <span data-ttu-id="f0ba7-126">аппдатафолдер</span><span class="sxs-lookup"><span data-stu-id="f0ba7-126">AppDataFolder</span></span>     | <span data-ttu-id="f0ba7-127">DataFolder2</span><span class="sxs-lookup"><span data-stu-id="f0ba7-127">DataFolder2</span></span> |



 

[<span data-ttu-id="f0ba7-128">Таблица Ремовефиле</span><span class="sxs-lookup"><span data-stu-id="f0ba7-128">RemoveFile Table</span></span>](removefile-table.md)



| <span data-ttu-id="f0ba7-129">филекэй</span><span class="sxs-lookup"><span data-stu-id="f0ba7-129">FileKey</span></span> | <span data-ttu-id="f0ba7-130">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="f0ba7-130">Component\_</span></span> | <span data-ttu-id="f0ba7-131">FileName</span><span class="sxs-lookup"><span data-stu-id="f0ba7-131">FileName</span></span> | <span data-ttu-id="f0ba7-132">дирпроперти</span><span class="sxs-lookup"><span data-stu-id="f0ba7-132">DirProperty</span></span> | <span data-ttu-id="f0ba7-133">InstallMode</span><span class="sxs-lookup"><span data-stu-id="f0ba7-133">InstallMode</span></span> |
|---------|-------------|----------|-------------|-------------|
| <span data-ttu-id="f0ba7-134">Key1</span><span class="sxs-lookup"><span data-stu-id="f0ba7-134">Key1</span></span>    | <span data-ttu-id="f0ba7-135">Component1</span><span class="sxs-lookup"><span data-stu-id="f0ba7-135">Component1</span></span>  |          | <span data-ttu-id="f0ba7-136">MyFolder</span><span class="sxs-lookup"><span data-stu-id="f0ba7-136">MyFolder</span></span>    | <span data-ttu-id="f0ba7-137">2</span><span class="sxs-lookup"><span data-stu-id="f0ba7-137">2</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="f0ba7-138">См. также</span><span class="sxs-lookup"><span data-stu-id="f0ba7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0ba7-139">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="f0ba7-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



