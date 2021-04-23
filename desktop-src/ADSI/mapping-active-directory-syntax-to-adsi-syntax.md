---
title: Сопоставление синтаксиса Active Directory синтаксису ADSI
description: Следующая таблица сопоставляет синтаксисы Active Directory с соответствующими синтаксисами ADSI.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- атрибуты ADSI, сопоставление синтаксиса Active Directory синтаксису ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654119"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a><span data-ttu-id="41ddd-104">Сопоставление синтаксиса Active Directory синтаксису ADSI</span><span class="sxs-lookup"><span data-stu-id="41ddd-104">Mapping Active Directory Syntax to ADSI Syntax</span></span>

<span data-ttu-id="41ddd-105">Следующая таблица сопоставляет синтаксисы Active Directory с соответствующими синтаксисами ADSI.</span><span class="sxs-lookup"><span data-stu-id="41ddd-105">The following table maps the Active Directory syntaxes to their corresponding ADSI syntaxes.</span></span>



| <span data-ttu-id="41ddd-106">Идентификатор синтаксиса атрибута</span><span class="sxs-lookup"><span data-stu-id="41ddd-106">Attribute syntax ID</span></span> | <span data-ttu-id="41ddd-107">Active Directory тип синтаксиса</span><span class="sxs-lookup"><span data-stu-id="41ddd-107">Active Directory syntax type</span></span>             | <span data-ttu-id="41ddd-108">Эквивалентный тип синтаксиса ADSI</span><span class="sxs-lookup"><span data-stu-id="41ddd-108">Equivalent ADSI syntax type</span></span>                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="41ddd-109">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="41ddd-109">2.5.5.1</span></span><br/>  | <span data-ttu-id="41ddd-110">Строка различающегося имени</span><span class="sxs-lookup"><span data-stu-id="41ddd-110">DN String</span></span><br/>                     | <span data-ttu-id="41ddd-111">Строка различающегося имени</span><span class="sxs-lookup"><span data-stu-id="41ddd-111">DN String</span></span><br/>                                                |
| <span data-ttu-id="41ddd-112">2.5.5.2</span><span class="sxs-lookup"><span data-stu-id="41ddd-112">2.5.5.2</span></span><br/>  | <span data-ttu-id="41ddd-113">Идентификатор объекта</span><span class="sxs-lookup"><span data-stu-id="41ddd-113">Object ID</span></span><br/>                     | <span data-ttu-id="41ddd-114">Строка Касеигноре</span><span class="sxs-lookup"><span data-stu-id="41ddd-114">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="41ddd-115">2.5.5.3</span><span class="sxs-lookup"><span data-stu-id="41ddd-115">2.5.5.3</span></span><br/>  | <span data-ttu-id="41ddd-116">Строка с учетом регистра</span><span class="sxs-lookup"><span data-stu-id="41ddd-116">Case Sensitive String</span></span><br/>         | <span data-ttu-id="41ddd-117">Строка Касиксакт</span><span class="sxs-lookup"><span data-stu-id="41ddd-117">CaseExact String</span></span><br/>                                         |
| <span data-ttu-id="41ddd-118">2.5.5.4</span><span class="sxs-lookup"><span data-stu-id="41ddd-118">2.5.5.4</span></span><br/>  | <span data-ttu-id="41ddd-119">Регистр пропущенных строк</span><span class="sxs-lookup"><span data-stu-id="41ddd-119">Case Ignored String</span></span><br/>           | <span data-ttu-id="41ddd-120">Строка Касеигноре</span><span class="sxs-lookup"><span data-stu-id="41ddd-120">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="41ddd-121">2.5.5.5</span><span class="sxs-lookup"><span data-stu-id="41ddd-121">2.5.5.5</span></span><br/>  | <span data-ttu-id="41ddd-122">Строка варианта печати</span><span class="sxs-lookup"><span data-stu-id="41ddd-122">Print Case String</span></span><br/>             | <span data-ttu-id="41ddd-123">Печатная строка</span><span class="sxs-lookup"><span data-stu-id="41ddd-123">Printable String</span></span><br/>                                         |
| <span data-ttu-id="41ddd-124">2.5.5.6</span><span class="sxs-lookup"><span data-stu-id="41ddd-124">2.5.5.6</span></span><br/>  | <span data-ttu-id="41ddd-125">Числовая строка</span><span class="sxs-lookup"><span data-stu-id="41ddd-125">Numeric String</span></span><br/>                | <span data-ttu-id="41ddd-126">Числовая строка</span><span class="sxs-lookup"><span data-stu-id="41ddd-126">Numeric String</span></span><br/>                                           |
| <span data-ttu-id="41ddd-127">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="41ddd-127">2.5.5.7</span></span><br/>  | <span data-ttu-id="41ddd-128">**Или** Имя Днвисоктетстринг</span><span class="sxs-lookup"><span data-stu-id="41ddd-128">**OR** Name DNWithOctetString</span></span><br/> | <span data-ttu-id="41ddd-129">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="41ddd-129">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="41ddd-130">2.5.5.8</span><span class="sxs-lookup"><span data-stu-id="41ddd-130">2.5.5.8</span></span><br/>  | <span data-ttu-id="41ddd-131">Логический</span><span class="sxs-lookup"><span data-stu-id="41ddd-131">Boolean</span></span><br/>                       | <span data-ttu-id="41ddd-132">Логический</span><span class="sxs-lookup"><span data-stu-id="41ddd-132">Boolean</span></span><br/>                                                  |
| <span data-ttu-id="41ddd-133">2.5.5.9</span><span class="sxs-lookup"><span data-stu-id="41ddd-133">2.5.5.9</span></span><br/>  | <span data-ttu-id="41ddd-134">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="41ddd-134">Integer</span></span><br/>                       | <span data-ttu-id="41ddd-135">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="41ddd-135">Integer</span></span><br/>                                                  |
| <span data-ttu-id="41ddd-136">2.5.5.10</span><span class="sxs-lookup"><span data-stu-id="41ddd-136">2.5.5.10</span></span><br/> | <span data-ttu-id="41ddd-137">Строка октета</span><span class="sxs-lookup"><span data-stu-id="41ddd-137">Octet String</span></span><br/>                  | <span data-ttu-id="41ddd-138">Строка октета</span><span class="sxs-lookup"><span data-stu-id="41ddd-138">Octet String</span></span><br/>                                             |
| <span data-ttu-id="41ddd-139">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="41ddd-139">2.5.5.11</span></span><br/> | <span data-ttu-id="41ddd-140">Время</span><span class="sxs-lookup"><span data-stu-id="41ddd-140">Time</span></span><br/>                          | <span data-ttu-id="41ddd-141">Время в формате UTC</span><span class="sxs-lookup"><span data-stu-id="41ddd-141">UTC Time</span></span><br/>                                                 |
| <span data-ttu-id="41ddd-142">2.5.5.12</span><span class="sxs-lookup"><span data-stu-id="41ddd-142">2.5.5.12</span></span><br/> | <span data-ttu-id="41ddd-143">Юникод</span><span class="sxs-lookup"><span data-stu-id="41ddd-143">Unicode</span></span><br/>                       | <span data-ttu-id="41ddd-144">Пропустить строку без учета регистра</span><span class="sxs-lookup"><span data-stu-id="41ddd-144">Case Ignore String</span></span><br/>                                       |
| <span data-ttu-id="41ddd-145">2.5.5.13</span><span class="sxs-lookup"><span data-stu-id="41ddd-145">2.5.5.13</span></span><br/> | <span data-ttu-id="41ddd-146">Адрес</span><span class="sxs-lookup"><span data-stu-id="41ddd-146">Address</span></span><br/>                       | <span data-ttu-id="41ddd-147">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="41ddd-147">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="41ddd-148">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="41ddd-148">2.5.5.14</span></span><br/> | <span data-ttu-id="41ddd-149">Distname-Address</span><span class="sxs-lookup"><span data-stu-id="41ddd-149">Distname-Address</span></span><br/>              |                                                                     |
| <span data-ttu-id="41ddd-150">2.5.5.15</span><span class="sxs-lookup"><span data-stu-id="41ddd-150">2.5.5.15</span></span><br/> | <span data-ttu-id="41ddd-151">Дескриптор безопасности NT</span><span class="sxs-lookup"><span data-stu-id="41ddd-151">NT Security Descriptor</span></span><br/>        | [<span data-ttu-id="41ddd-152">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="41ddd-152">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| <span data-ttu-id="41ddd-153">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="41ddd-153">2.5.5.16</span></span><br/> | <span data-ttu-id="41ddd-154">Большое целое число</span><span class="sxs-lookup"><span data-stu-id="41ddd-154">Large Integer</span></span><br/>                 | [<span data-ttu-id="41ddd-155">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="41ddd-155">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| <span data-ttu-id="41ddd-156">2.5.5.17</span><span class="sxs-lookup"><span data-stu-id="41ddd-156">2.5.5.17</span></span><br/> | <span data-ttu-id="41ddd-157">SID</span><span class="sxs-lookup"><span data-stu-id="41ddd-157">SID</span></span><br/>                           | <span data-ttu-id="41ddd-158">Строка октета</span><span class="sxs-lookup"><span data-stu-id="41ddd-158">Octet String</span></span><br/>                                             |



 

 

 





