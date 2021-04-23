---
title: Атрибут ms-DS-User-encrypted-Text-Password-Allowed
description: Указывает, будет ли Active Directory хранить пароль в формате обратимого шифрования.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута Active-DS-User-encrypted-Text-Password
- Схема AD атрибута ms-DS-Усеренкриптедтекстпассвордалловед
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493569"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a><span data-ttu-id="7d2dd-105">Атрибут ms-DS-User-encrypted-Text-Password-Allowed</span><span class="sxs-lookup"><span data-stu-id="7d2dd-105">ms-DS-User-Encrypted-Text-Password-Allowed attribute</span></span>

<span data-ttu-id="7d2dd-106">Указывает, будет ли Active Directory хранить пароль в формате обратимого шифрования.</span><span class="sxs-lookup"><span data-stu-id="7d2dd-106">Indicates whether Active Directory will store the password in the reversible encryption format.</span></span> <span data-ttu-id="7d2dd-107">Значение true, если пароль хранится в формате обратимого шифрования; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="7d2dd-107">True if the password is stored in the reversible encryption format; otherwise, False.</span></span>

> [!Note]  
> <span data-ttu-id="7d2dd-108">Этот атрибут не используется [службы Active Directory облегченного доступа к каталогам](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) и включается только для полноты или контроля четности с помощью userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="7d2dd-108">This attribute is not used by [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) and is only included for completeness/parity with userAccountControl.</span></span> <span data-ttu-id="7d2dd-109">AD LDS не сохраняет пароли с обратимым шифрованием независимо от значения этого атрибута на любом заданном объекте или политики безопасности компьютера, относящейся к обратимому шифрованию самого компьютера.</span><span class="sxs-lookup"><span data-stu-id="7d2dd-109">AD LDS does not store passwords with reversible encryption, regardless of this attribute's value on any given object or the computer security policy pertaining to reversible encryption on the computer itself.</span></span>

 



| <span data-ttu-id="7d2dd-110">Ввод</span><span class="sxs-lookup"><span data-stu-id="7d2dd-110">Entry</span></span> | <span data-ttu-id="7d2dd-111">Значение</span><span class="sxs-lookup"><span data-stu-id="7d2dd-111">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="7d2dd-112">CN</span><span class="sxs-lookup"><span data-stu-id="7d2dd-112">CN</span></span>                | <span data-ttu-id="7d2dd-113">MS-DS-User-encrypted-Text-Password-Allowed</span><span class="sxs-lookup"><span data-stu-id="7d2dd-113">ms-DS-User-Encrypted-Text-Password-Allowed</span></span> |
| <span data-ttu-id="7d2dd-114">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7d2dd-114">Ldap-Display-Name</span></span> | <span data-ttu-id="7d2dd-115">MS-DS-Усеренкриптедтекстпассвордалловед</span><span class="sxs-lookup"><span data-stu-id="7d2dd-115">ms-DS-UserEncryptedTextPasswordAllowed</span></span>     |
| <span data-ttu-id="7d2dd-116">Размер</span><span class="sxs-lookup"><span data-stu-id="7d2dd-116">Size</span></span>              | \-                                         |
| <span data-ttu-id="7d2dd-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7d2dd-117">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="7d2dd-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7d2dd-118">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="7d2dd-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7d2dd-119">Attribute-Id</span></span>      | <span data-ttu-id="7d2dd-120">1.2.840.113556.1.4.1856</span><span class="sxs-lookup"><span data-stu-id="7d2dd-120">1.2.840.113556.1.4.1856</span></span>                    |
| <span data-ttu-id="7d2dd-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7d2dd-121">System-Id-Guid</span></span>    | <span data-ttu-id="7d2dd-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span><span class="sxs-lookup"><span data-stu-id="7d2dd-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span></span>       |
| <span data-ttu-id="7d2dd-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d2dd-123">Syntax</span></span>            | [<span data-ttu-id="7d2dd-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="7d2dd-124">**Boolean**</span></span>](s-boolean.md)               |



## <a name="implementations"></a><span data-ttu-id="7d2dd-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7d2dd-125">Implementations</span></span>

-   [<span data-ttu-id="7d2dd-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7d2dd-126">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="7d2dd-127">ADAM</span><span class="sxs-lookup"><span data-stu-id="7d2dd-127">ADAM</span></span>



| <span data-ttu-id="7d2dd-128">Ввод</span><span class="sxs-lookup"><span data-stu-id="7d2dd-128">Entry</span></span> | <span data-ttu-id="7d2dd-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7d2dd-129">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7d2dd-130">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7d2dd-130">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7d2dd-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d2dd-131">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7d2dd-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d2dd-132">System-Only</span></span>            | <span data-ttu-id="7d2dd-133">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d2dd-133">False</span></span>                                                             |
| <span data-ttu-id="7d2dd-134">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7d2dd-134">Is-Single-Valued</span></span>       | <span data-ttu-id="7d2dd-135">True</span><span class="sxs-lookup"><span data-stu-id="7d2dd-135">True</span></span>                                                              |
| <span data-ttu-id="7d2dd-136">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7d2dd-136">Is Indexed</span></span>             | <span data-ttu-id="7d2dd-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d2dd-137">False</span></span>                                                             |
| <span data-ttu-id="7d2dd-138">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7d2dd-138">In Global Catalog</span></span>      | <span data-ttu-id="7d2dd-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d2dd-139">False</span></span>                                                             |
| <span data-ttu-id="7d2dd-140">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7d2dd-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d2dd-141">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7d2dd-141">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="7d2dd-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d2dd-142">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="7d2dd-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d2dd-143">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="7d2dd-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d2dd-144">Search-Flags</span></span>           | <span data-ttu-id="7d2dd-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d2dd-145">0x00000000</span></span>                                                        |
| <span data-ttu-id="7d2dd-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d2dd-146">System-Flags</span></span>           | <span data-ttu-id="7d2dd-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d2dd-147">0x00000010</span></span>                                                        |
| <span data-ttu-id="7d2dd-148">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7d2dd-148">Classes used in</span></span>        | [<span data-ttu-id="7d2dd-149">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="7d2dd-149">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7d2dd-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d2dd-150">Remarks</span></span>

<span data-ttu-id="7d2dd-151">В ADAM этот атрибут заменяет флаг " [**ADS \_ УФ \_ Encrypted \_ Text \_ password \_**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) " для атрибута [**userAccountControl**](a-useraccountcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="7d2dd-151">In ADAM, this attribute replaces the [**ADS\_UF\_ENCRYPTED\_TEXT\_PASSWORD\_ALLOWED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

