---
title: Расширенное право на проверку подлинности
description: Элемент управления право доступа контролирует, кто может проходить проверку подлинности на определенном компьютере или в службе.
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- Расширенная правая схема AD, разрешенная для проверки подлинности
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2fca1b6f4670fd340170ed5cfd1f0160d61945
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494085"
---
# <a name="allowed-to-authenticate-extended-right"></a><span data-ttu-id="50a99-104">Расширенное право на проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="50a99-104">Allowed-To-Authenticate extended right</span></span>

<span data-ttu-id="50a99-105">Элемент управления право доступа контролирует, кто может проходить проверку подлинности на определенном компьютере или в службе.</span><span class="sxs-lookup"><span data-stu-id="50a99-105">The control access right controls who can authenticate to a particular computer or service.</span></span> <span data-ttu-id="50a99-106">По сути, оно находится на объектах Computer, User и InetOrgPerson.</span><span class="sxs-lookup"><span data-stu-id="50a99-106">It basically lives on computer, user, and InetOrgPerson objects.</span></span> <span data-ttu-id="50a99-107">Он также применяется к объекту домена, если доступ разрешен для всего домена.</span><span class="sxs-lookup"><span data-stu-id="50a99-107">It is also applicable on the domain object if access is allowed for the entire domain.</span></span> <span data-ttu-id="50a99-108">Его можно применить к подразделениям, чтобы пользователи могли устанавливать наследуемые ACE для подразделений, содержащих набор объектов User или Computer.</span><span class="sxs-lookup"><span data-stu-id="50a99-108">It can be applied to OUs to permit users to be able to set inheritable ACEs on OUs that contain a set of user or computer objects.</span></span>



| <span data-ttu-id="50a99-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="50a99-109">Entry</span></span> | <span data-ttu-id="50a99-110">Значение</span><span class="sxs-lookup"><span data-stu-id="50a99-110">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="50a99-111">CN</span><span class="sxs-lookup"><span data-stu-id="50a99-111">CN</span></span>           | <span data-ttu-id="50a99-112">Разрешено — проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="50a99-112">Allowed-To-Authenticate</span></span>              |
| <span data-ttu-id="50a99-113">Display-Name</span><span class="sxs-lookup"><span data-stu-id="50a99-113">Display-Name</span></span> | <span data-ttu-id="50a99-114">Разрешена проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="50a99-114">Allowed to Authenticate</span></span>              |
| <span data-ttu-id="50a99-115">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="50a99-115">Rights-GUID</span></span>  | <span data-ttu-id="50a99-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span><span class="sxs-lookup"><span data-stu-id="50a99-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span></span> |



## <a name="implementations"></a><span data-ttu-id="50a99-117">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="50a99-117">Implementations</span></span>

-   [<span data-ttu-id="50a99-118">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="50a99-118">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="50a99-119">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="50a99-119">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="50a99-120">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="50a99-120">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="50a99-121">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="50a99-121">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="50a99-122">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="50a99-122">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="50a99-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="50a99-123">Windows Server 2003</span></span>



| <span data-ttu-id="50a99-124">Ввод</span><span class="sxs-lookup"><span data-stu-id="50a99-124">Entry</span></span> | <span data-ttu-id="50a99-125">Значение</span><span class="sxs-lookup"><span data-stu-id="50a99-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a99-126">Applies-To</span><span class="sxs-lookup"><span data-stu-id="50a99-126">Applies-To</span></span>              | [<span data-ttu-id="50a99-127">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="50a99-127">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="50a99-128">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="50a99-128">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="50a99-129">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="50a99-129">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="50a99-130">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="50a99-130">Localization-Display-ID</span></span> | <span data-ttu-id="50a99-131">65</span><span class="sxs-lookup"><span data-stu-id="50a99-131">65</span></span>                                                                                                                              |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="50a99-132">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="50a99-132">Windows Server 2003 R2</span></span>



| <span data-ttu-id="50a99-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="50a99-133">Entry</span></span> | <span data-ttu-id="50a99-134">Значение</span><span class="sxs-lookup"><span data-stu-id="50a99-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a99-135">Applies-To</span><span class="sxs-lookup"><span data-stu-id="50a99-135">Applies-To</span></span>              | [<span data-ttu-id="50a99-136">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="50a99-136">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="50a99-137">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="50a99-137">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="50a99-138">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="50a99-138">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="50a99-139">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="50a99-139">Localization-Display-ID</span></span> | <span data-ttu-id="50a99-140">65</span><span class="sxs-lookup"><span data-stu-id="50a99-140">65</span></span>                                                                                                                              |



## <a name="windows-server-2008"></a><span data-ttu-id="50a99-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50a99-141">Windows Server 2008</span></span>



| <span data-ttu-id="50a99-142">Ввод</span><span class="sxs-lookup"><span data-stu-id="50a99-142">Entry</span></span> | <span data-ttu-id="50a99-143">Значение</span><span class="sxs-lookup"><span data-stu-id="50a99-143">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a99-144">Applies-To</span><span class="sxs-lookup"><span data-stu-id="50a99-144">Applies-To</span></span>              | [<span data-ttu-id="50a99-145">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="50a99-145">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="50a99-146">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="50a99-146">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="50a99-147">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="50a99-147">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="50a99-148">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="50a99-148">Localization-Display-ID</span></span> | <span data-ttu-id="50a99-149">65</span><span class="sxs-lookup"><span data-stu-id="50a99-149">65</span></span>                                                                                                                              |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="50a99-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50a99-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="50a99-151">Ввод</span><span class="sxs-lookup"><span data-stu-id="50a99-151">Entry</span></span> | <span data-ttu-id="50a99-152">Значение</span><span class="sxs-lookup"><span data-stu-id="50a99-152">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a99-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="50a99-153">Applies-To</span></span>              | [<span data-ttu-id="50a99-154">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="50a99-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="50a99-155">**Учетная запись MS-DS-Managed-Service-**</span><span class="sxs-lookup"><span data-stu-id="50a99-155">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="50a99-156">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="50a99-156">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="50a99-157">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="50a99-157">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="50a99-158">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="50a99-158">Localization-Display-ID</span></span> | <span data-ttu-id="50a99-159">65</span><span class="sxs-lookup"><span data-stu-id="50a99-159">65</span></span>                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a><span data-ttu-id="50a99-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50a99-160">Windows Server 2012</span></span>



| <span data-ttu-id="50a99-161">Ввод</span><span class="sxs-lookup"><span data-stu-id="50a99-161">Entry</span></span> | <span data-ttu-id="50a99-162">Значение</span><span class="sxs-lookup"><span data-stu-id="50a99-162">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a99-163">Applies-To</span><span class="sxs-lookup"><span data-stu-id="50a99-163">Applies-To</span></span>              | [<span data-ttu-id="50a99-164">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="50a99-164">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="50a99-165">**Учетная запись MS-DS-Managed-Service-**</span><span class="sxs-lookup"><span data-stu-id="50a99-165">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="50a99-166">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="50a99-166">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="50a99-167">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="50a99-167">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="50a99-168">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="50a99-168">Localization-Display-ID</span></span> | <span data-ttu-id="50a99-169">65</span><span class="sxs-lookup"><span data-stu-id="50a99-169">65</span></span>                                                                                                                                                                                                               |



 

 





