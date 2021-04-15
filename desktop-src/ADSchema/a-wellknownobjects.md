---
title: Атрибут "хорошо известные объекты"
description: Этот атрибут содержит список хорошо известных контейнеров объектов по идентификатору GUID и различающееся имя.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов хорошо известных объектов
- Схема AD атрибута Веллкновнобжектс
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493899"
---
# <a name="well-known-objects-attribute"></a><span data-ttu-id="d8938-105">Атрибут "хорошо известные объекты"</span><span class="sxs-lookup"><span data-stu-id="d8938-105">Well-Known-Objects attribute</span></span>

<span data-ttu-id="d8938-106">Этот атрибут содержит список хорошо известных контейнеров объектов по идентификатору GUID и различающееся имя.</span><span class="sxs-lookup"><span data-stu-id="d8938-106">This attribute contains a list of well-known object containers by GUID and distinguished name.</span></span> <span data-ttu-id="d8938-107">Хорошо известные объекты являются системными контейнерами.</span><span class="sxs-lookup"><span data-stu-id="d8938-107">The well-known objects are system containers.</span></span> <span data-ttu-id="d8938-108">Эти сведения используются для получения объекта после перемещения с использованием только идентификатора GUID и имени домена.</span><span class="sxs-lookup"><span data-stu-id="d8938-108">This information is used to retrieve an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="d8938-109">При перемещении объекта система автоматически обновляет часть различающегося имени в значениях известных объектов, которые ссылаются на объект.</span><span class="sxs-lookup"><span data-stu-id="d8938-109">Whenever the object is moved, the system automatically updates the Distinguished Name portion of the Well-Known-Objects values that referred to the object.</span></span> <span data-ttu-id="d8938-110">Файл NTDSAPI. h содержит следующие определения, которые можно использовать для получения объекта (идентификаторы GUID, связанные с этими объектами, содержатся в NTDSAPI. h):</span><span class="sxs-lookup"><span data-stu-id="d8938-110">The file Ntdsapi.h contains the following definitions, which can be used to retrieve an object (the GUIDs that are associated to these objects are contained in Ntdsapi.h):</span></span>

-   <span data-ttu-id="d8938-111">контейнер пользователей с идентификаторами GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="d8938-111">GUID\_USERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d8938-112">GUID \_ компутрс \_ контейнер \_ W</span><span class="sxs-lookup"><span data-stu-id="d8938-112">GUID\_COMPUTRS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d8938-113">Идентификатор \_ системы GUID, \_ контейнер \_</span><span class="sxs-lookup"><span data-stu-id="d8938-113">GUID\_SYSTEMS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d8938-114">GUID \_ \_ контроллеров домена, \_ контейнер \_</span><span class="sxs-lookup"><span data-stu-id="d8938-114">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d8938-115">\_контейнер инфраструктуры \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="d8938-115">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d8938-116">GUID \_ удаленных \_ объектов, \_ контейнер \_</span><span class="sxs-lookup"><span data-stu-id="d8938-116">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d8938-117">GUID \_ LOSTANDFOUND \_ контейнера \_ W</span><span class="sxs-lookup"><span data-stu-id="d8938-117">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d8938-118">GUID \_ FOREIGNSECURITYPRINCIPALS \_ контейнер \_ W</span><span class="sxs-lookup"><span data-stu-id="d8938-118">GUID\_FOREIGNSECURITYPRINCIPALS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d8938-119">\_контейнер данных программы для идентификатора GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="d8938-119">GUID\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d8938-120">GUID \_ \_ \_ контейнер данных программы \_ Майкрософт \_ W</span><span class="sxs-lookup"><span data-stu-id="d8938-120">GUID\_MICROSOFT\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d8938-121">GUID \_ . \_ контейнер квот \_ NTDS \_ W</span><span class="sxs-lookup"><span data-stu-id="d8938-121">GUID\_NTDS\_QUOTAS\_CONTAINER\_W</span></span>



| <span data-ttu-id="d8938-122">Ввод</span><span class="sxs-lookup"><span data-stu-id="d8938-122">Entry</span></span> | <span data-ttu-id="d8938-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d8938-123">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="d8938-124">CN</span><span class="sxs-lookup"><span data-stu-id="d8938-124">CN</span></span>                | <span data-ttu-id="d8938-125">Хорошо известные объекты</span><span class="sxs-lookup"><span data-stu-id="d8938-125">Well-Known-Objects</span></span>                              |
| <span data-ttu-id="d8938-126">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d8938-126">Ldap-Display-Name</span></span> | <span data-ttu-id="d8938-127">веллкновнобжектс</span><span class="sxs-lookup"><span data-stu-id="d8938-127">wellKnownObjects</span></span>                                |
| <span data-ttu-id="d8938-128">Размер</span><span class="sxs-lookup"><span data-stu-id="d8938-128">Size</span></span>              | \-                                              |
| <span data-ttu-id="d8938-129">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d8938-129">Update Privilege</span></span>  | <span data-ttu-id="d8938-130">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="d8938-130">This value is set by the system.</span></span>                |
| <span data-ttu-id="d8938-131">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d8938-131">Update Frequency</span></span>  | <span data-ttu-id="d8938-132">При перемещении одного из системных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="d8938-132">Whenever one of the system containers is moved.</span></span> |
| <span data-ttu-id="d8938-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d8938-133">Attribute-Id</span></span>      | <span data-ttu-id="d8938-134">1.2.840.113556.1.4.618</span><span class="sxs-lookup"><span data-stu-id="d8938-134">1.2.840.113556.1.4.618</span></span>                          |
| <span data-ttu-id="d8938-135">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d8938-135">System-Id-Guid</span></span>    | <span data-ttu-id="d8938-136">05308983-7688-11d1-aded-00c04fd8d5cd</span><span class="sxs-lookup"><span data-stu-id="d8938-136">05308983-7688-11d1-aded-00c04fd8d5cd</span></span>            |
| <span data-ttu-id="d8938-137">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8938-137">Syntax</span></span>            | [<span data-ttu-id="d8938-138">**Object(двоичный_DN)**</span><span class="sxs-lookup"><span data-stu-id="d8938-138">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="d8938-139">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d8938-139">Implementations</span></span>

-   [<span data-ttu-id="d8938-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d8938-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d8938-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d8938-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d8938-142">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d8938-142">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d8938-143">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d8938-143">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d8938-144">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d8938-144">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d8938-145">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d8938-145">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d8938-146">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d8938-146">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d8938-147">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d8938-147">Windows 2000 Server</span></span>



| <span data-ttu-id="d8938-148">Ввод</span><span class="sxs-lookup"><span data-stu-id="d8938-148">Entry</span></span> | <span data-ttu-id="d8938-149">Значение</span><span class="sxs-lookup"><span data-stu-id="d8938-149">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d8938-150">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d8938-150">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-151">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8938-151">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-152">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8938-152">System-Only</span></span>            | <span data-ttu-id="d8938-153">True</span><span class="sxs-lookup"><span data-stu-id="d8938-153">True</span></span>                            |
| <span data-ttu-id="d8938-154">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d8938-154">Is-Single-Valued</span></span>       | <span data-ttu-id="d8938-155">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-155">False</span></span>                           |
| <span data-ttu-id="d8938-156">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d8938-156">Is Indexed</span></span>             | <span data-ttu-id="d8938-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-157">False</span></span>                           |
| <span data-ttu-id="d8938-158">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d8938-158">In Global Catalog</span></span>      | <span data-ttu-id="d8938-159">True</span><span class="sxs-lookup"><span data-stu-id="d8938-159">True</span></span>                            |
| <span data-ttu-id="d8938-160">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d8938-160">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8938-161">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d8938-161">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d8938-162">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8938-162">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d8938-163">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8938-163">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d8938-164">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-164">Search-Flags</span></span>           | <span data-ttu-id="d8938-165">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d8938-165">0x00000000</span></span>                      |
| <span data-ttu-id="d8938-166">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-166">System-Flags</span></span>           | <span data-ttu-id="d8938-167">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d8938-167">0x00000012</span></span>                      |
| <span data-ttu-id="d8938-168">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d8938-168">Classes used in</span></span>        | [<span data-ttu-id="d8938-169">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d8938-169">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d8938-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d8938-170">Windows Server 2003</span></span>



| <span data-ttu-id="d8938-171">Ввод</span><span class="sxs-lookup"><span data-stu-id="d8938-171">Entry</span></span> | <span data-ttu-id="d8938-172">Значение</span><span class="sxs-lookup"><span data-stu-id="d8938-172">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d8938-173">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d8938-173">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-174">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8938-174">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-175">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8938-175">System-Only</span></span>            | <span data-ttu-id="d8938-176">True</span><span class="sxs-lookup"><span data-stu-id="d8938-176">True</span></span>                            |
| <span data-ttu-id="d8938-177">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d8938-177">Is-Single-Valued</span></span>       | <span data-ttu-id="d8938-178">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-178">False</span></span>                           |
| <span data-ttu-id="d8938-179">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d8938-179">Is Indexed</span></span>             | <span data-ttu-id="d8938-180">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-180">False</span></span>                           |
| <span data-ttu-id="d8938-181">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d8938-181">In Global Catalog</span></span>      | <span data-ttu-id="d8938-182">True</span><span class="sxs-lookup"><span data-stu-id="d8938-182">True</span></span>                            |
| <span data-ttu-id="d8938-183">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d8938-183">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8938-184">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d8938-184">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d8938-185">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8938-185">Range-Lower</span></span>            | <span data-ttu-id="d8938-186">16</span><span class="sxs-lookup"><span data-stu-id="d8938-186">16</span></span>                              |
| <span data-ttu-id="d8938-187">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8938-187">Range-Upper</span></span>            | <span data-ttu-id="d8938-188">16</span><span class="sxs-lookup"><span data-stu-id="d8938-188">16</span></span>                              |
| <span data-ttu-id="d8938-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-189">Search-Flags</span></span>           | <span data-ttu-id="d8938-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d8938-190">0x00000000</span></span>                      |
| <span data-ttu-id="d8938-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-191">System-Flags</span></span>           | <span data-ttu-id="d8938-192">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d8938-192">0x00000012</span></span>                      |
| <span data-ttu-id="d8938-193">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d8938-193">Classes used in</span></span>        | [<span data-ttu-id="d8938-194">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d8938-194">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d8938-195">ADAM</span><span class="sxs-lookup"><span data-stu-id="d8938-195">ADAM</span></span>



| <span data-ttu-id="d8938-196">Ввод</span><span class="sxs-lookup"><span data-stu-id="d8938-196">Entry</span></span> | <span data-ttu-id="d8938-197">Значение</span><span class="sxs-lookup"><span data-stu-id="d8938-197">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d8938-198">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d8938-198">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8938-199">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8938-200">System-Only</span></span>            | <span data-ttu-id="d8938-201">True</span><span class="sxs-lookup"><span data-stu-id="d8938-201">True</span></span>                            |
| <span data-ttu-id="d8938-202">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d8938-202">Is-Single-Valued</span></span>       | <span data-ttu-id="d8938-203">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-203">False</span></span>                           |
| <span data-ttu-id="d8938-204">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d8938-204">Is Indexed</span></span>             | <span data-ttu-id="d8938-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-205">False</span></span>                           |
| <span data-ttu-id="d8938-206">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d8938-206">In Global Catalog</span></span>      | <span data-ttu-id="d8938-207">True</span><span class="sxs-lookup"><span data-stu-id="d8938-207">True</span></span>                            |
| <span data-ttu-id="d8938-208">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d8938-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8938-209">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d8938-209">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d8938-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8938-210">Range-Lower</span></span>            | <span data-ttu-id="d8938-211">16</span><span class="sxs-lookup"><span data-stu-id="d8938-211">16</span></span>                              |
| <span data-ttu-id="d8938-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8938-212">Range-Upper</span></span>            | <span data-ttu-id="d8938-213">16</span><span class="sxs-lookup"><span data-stu-id="d8938-213">16</span></span>                              |
| <span data-ttu-id="d8938-214">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-214">Search-Flags</span></span>           | <span data-ttu-id="d8938-215">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d8938-215">0x00000000</span></span>                      |
| <span data-ttu-id="d8938-216">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-216">System-Flags</span></span>           | <span data-ttu-id="d8938-217">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d8938-217">0x00000012</span></span>                      |
| <span data-ttu-id="d8938-218">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d8938-218">Classes used in</span></span>        | [<span data-ttu-id="d8938-219">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d8938-219">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d8938-220">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d8938-220">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d8938-221">Ввод</span><span class="sxs-lookup"><span data-stu-id="d8938-221">Entry</span></span> | <span data-ttu-id="d8938-222">Значение</span><span class="sxs-lookup"><span data-stu-id="d8938-222">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d8938-223">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d8938-223">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8938-224">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8938-225">System-Only</span></span>            | <span data-ttu-id="d8938-226">True</span><span class="sxs-lookup"><span data-stu-id="d8938-226">True</span></span>                            |
| <span data-ttu-id="d8938-227">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d8938-227">Is-Single-Valued</span></span>       | <span data-ttu-id="d8938-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-228">False</span></span>                           |
| <span data-ttu-id="d8938-229">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d8938-229">Is Indexed</span></span>             | <span data-ttu-id="d8938-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-230">False</span></span>                           |
| <span data-ttu-id="d8938-231">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d8938-231">In Global Catalog</span></span>      | <span data-ttu-id="d8938-232">True</span><span class="sxs-lookup"><span data-stu-id="d8938-232">True</span></span>                            |
| <span data-ttu-id="d8938-233">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d8938-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8938-234">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d8938-234">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d8938-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8938-235">Range-Lower</span></span>            | <span data-ttu-id="d8938-236">16</span><span class="sxs-lookup"><span data-stu-id="d8938-236">16</span></span>                              |
| <span data-ttu-id="d8938-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8938-237">Range-Upper</span></span>            | <span data-ttu-id="d8938-238">16</span><span class="sxs-lookup"><span data-stu-id="d8938-238">16</span></span>                              |
| <span data-ttu-id="d8938-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-239">Search-Flags</span></span>           | <span data-ttu-id="d8938-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d8938-240">0x00000000</span></span>                      |
| <span data-ttu-id="d8938-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-241">System-Flags</span></span>           | <span data-ttu-id="d8938-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d8938-242">0x00000012</span></span>                      |
| <span data-ttu-id="d8938-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d8938-243">Classes used in</span></span>        | [<span data-ttu-id="d8938-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d8938-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d8938-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8938-245">Windows Server 2008</span></span>



| <span data-ttu-id="d8938-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="d8938-246">Entry</span></span> | <span data-ttu-id="d8938-247">Значение</span><span class="sxs-lookup"><span data-stu-id="d8938-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d8938-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d8938-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8938-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8938-250">System-Only</span></span>            | <span data-ttu-id="d8938-251">True</span><span class="sxs-lookup"><span data-stu-id="d8938-251">True</span></span>                            |
| <span data-ttu-id="d8938-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d8938-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d8938-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-253">False</span></span>                           |
| <span data-ttu-id="d8938-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d8938-254">Is Indexed</span></span>             | <span data-ttu-id="d8938-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-255">False</span></span>                           |
| <span data-ttu-id="d8938-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d8938-256">In Global Catalog</span></span>      | <span data-ttu-id="d8938-257">True</span><span class="sxs-lookup"><span data-stu-id="d8938-257">True</span></span>                            |
| <span data-ttu-id="d8938-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d8938-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8938-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d8938-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d8938-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8938-260">Range-Lower</span></span>            | <span data-ttu-id="d8938-261">16</span><span class="sxs-lookup"><span data-stu-id="d8938-261">16</span></span>                              |
| <span data-ttu-id="d8938-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8938-262">Range-Upper</span></span>            | <span data-ttu-id="d8938-263">16</span><span class="sxs-lookup"><span data-stu-id="d8938-263">16</span></span>                              |
| <span data-ttu-id="d8938-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-264">Search-Flags</span></span>           | <span data-ttu-id="d8938-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d8938-265">0x00000000</span></span>                      |
| <span data-ttu-id="d8938-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-266">System-Flags</span></span>           | <span data-ttu-id="d8938-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d8938-267">0x00000012</span></span>                      |
| <span data-ttu-id="d8938-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d8938-268">Classes used in</span></span>        | [<span data-ttu-id="d8938-269">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d8938-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d8938-270">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d8938-270">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d8938-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="d8938-271">Entry</span></span> | <span data-ttu-id="d8938-272">Значение</span><span class="sxs-lookup"><span data-stu-id="d8938-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d8938-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d8938-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8938-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8938-275">System-Only</span></span>            | <span data-ttu-id="d8938-276">True</span><span class="sxs-lookup"><span data-stu-id="d8938-276">True</span></span>                            |
| <span data-ttu-id="d8938-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d8938-277">Is-Single-Valued</span></span>       | <span data-ttu-id="d8938-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-278">False</span></span>                           |
| <span data-ttu-id="d8938-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d8938-279">Is Indexed</span></span>             | <span data-ttu-id="d8938-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-280">False</span></span>                           |
| <span data-ttu-id="d8938-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d8938-281">In Global Catalog</span></span>      | <span data-ttu-id="d8938-282">True</span><span class="sxs-lookup"><span data-stu-id="d8938-282">True</span></span>                            |
| <span data-ttu-id="d8938-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d8938-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8938-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d8938-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d8938-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8938-285">Range-Lower</span></span>            | <span data-ttu-id="d8938-286">16</span><span class="sxs-lookup"><span data-stu-id="d8938-286">16</span></span>                              |
| <span data-ttu-id="d8938-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8938-287">Range-Upper</span></span>            | <span data-ttu-id="d8938-288">16</span><span class="sxs-lookup"><span data-stu-id="d8938-288">16</span></span>                              |
| <span data-ttu-id="d8938-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-289">Search-Flags</span></span>           | <span data-ttu-id="d8938-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d8938-290">0x00000000</span></span>                      |
| <span data-ttu-id="d8938-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-291">System-Flags</span></span>           | <span data-ttu-id="d8938-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d8938-292">0x00000012</span></span>                      |
| <span data-ttu-id="d8938-293">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d8938-293">Classes used in</span></span>        | [<span data-ttu-id="d8938-294">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d8938-294">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d8938-295">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d8938-295">Windows Server 2012</span></span>



| <span data-ttu-id="d8938-296">Ввод</span><span class="sxs-lookup"><span data-stu-id="d8938-296">Entry</span></span> | <span data-ttu-id="d8938-297">Значение</span><span class="sxs-lookup"><span data-stu-id="d8938-297">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d8938-298">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d8938-298">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-299">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8938-299">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d8938-300">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8938-300">System-Only</span></span>            | <span data-ttu-id="d8938-301">True</span><span class="sxs-lookup"><span data-stu-id="d8938-301">True</span></span>                            |
| <span data-ttu-id="d8938-302">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d8938-302">Is-Single-Valued</span></span>       | <span data-ttu-id="d8938-303">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-303">False</span></span>                           |
| <span data-ttu-id="d8938-304">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d8938-304">Is Indexed</span></span>             | <span data-ttu-id="d8938-305">Неверно</span><span class="sxs-lookup"><span data-stu-id="d8938-305">False</span></span>                           |
| <span data-ttu-id="d8938-306">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d8938-306">In Global Catalog</span></span>      | <span data-ttu-id="d8938-307">True</span><span class="sxs-lookup"><span data-stu-id="d8938-307">True</span></span>                            |
| <span data-ttu-id="d8938-308">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d8938-308">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8938-309">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d8938-309">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d8938-310">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8938-310">Range-Lower</span></span>            | <span data-ttu-id="d8938-311">16</span><span class="sxs-lookup"><span data-stu-id="d8938-311">16</span></span>                              |
| <span data-ttu-id="d8938-312">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8938-312">Range-Upper</span></span>            | <span data-ttu-id="d8938-313">16</span><span class="sxs-lookup"><span data-stu-id="d8938-313">16</span></span>                              |
| <span data-ttu-id="d8938-314">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-314">Search-Flags</span></span>           | <span data-ttu-id="d8938-315">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d8938-315">0x00000000</span></span>                      |
| <span data-ttu-id="d8938-316">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8938-316">System-Flags</span></span>           | <span data-ttu-id="d8938-317">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d8938-317">0x00000012</span></span>                      |
| <span data-ttu-id="d8938-318">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d8938-318">Classes used in</span></span>        | [<span data-ttu-id="d8938-319">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d8938-319">**Top**</span></span>](c-top.md)<br/> |



 

 





