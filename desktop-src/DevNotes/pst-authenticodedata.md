---
description: Определяет данные для использования в проверке Microsoft Authenticode данных элемента.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: Структура PST_AUTHENTICODEDATA (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648727"
---
# <a name="pst_authenticodedata-structure"></a><span data-ttu-id="19d1f-103">\_Структура PST аусентикодедата</span><span class="sxs-lookup"><span data-stu-id="19d1f-103">PST\_AUTHENTICODEDATA structure</span></span>

<span data-ttu-id="19d1f-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="19d1f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="19d1f-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="19d1f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="19d1f-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="19d1f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="19d1f-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="19d1f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="19d1f-108">Определяет данные для использования в проверке Microsoft Authenticode данных элемента.</span><span class="sxs-lookup"><span data-stu-id="19d1f-108">Defines data to be used in Microsoft Authenticode verification of item data.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d1f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19d1f-109">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a><span data-ttu-id="19d1f-110">Члены</span><span class="sxs-lookup"><span data-stu-id="19d1f-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="19d1f-111">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="19d1f-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="19d1f-112">Размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="19d1f-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="19d1f-113">**двмодифиерс**</span><span class="sxs-lookup"><span data-stu-id="19d1f-113">**dwModifiers**</span></span>
</dt> <dd>

<span data-ttu-id="19d1f-114">Значение, идентифицирующее модификатор, который должен быть проверен одной из цепочек вызывающих объектов.</span><span class="sxs-lookup"><span data-stu-id="19d1f-114">A value that identifies the modifier that one of a chain of callers must verify.</span></span>



| <span data-ttu-id="19d1f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="19d1f-115">Value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="19d1f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="19d1f-116">Meaning</span></span>                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <span data-ttu-id="19d1f-117">PST-файл <dt>**\_ \_Один \_ вызывающий объект AC**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="19d1f-117"><dt>**PST\_AC\_SINGLE\_CALLER**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="19d1f-118">PStore только один уровень в цепочке вызовов.</span><span class="sxs-lookup"><span data-stu-id="19d1f-118">Only a single level in the call chain to PStore.</span></span> <span data-ttu-id="19d1f-119">Вызывающий объект проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="19d1f-119">The caller passes the verification check.</span></span> <span data-ttu-id="19d1f-120">Указанный образ является непосредственным вызывающим объектом, а — приложением (. exe).</span><span class="sxs-lookup"><span data-stu-id="19d1f-120">The specified image is the immediate caller, and is an application (.exe).</span></span><br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <span data-ttu-id="19d1f-121">PST-файл <dt>**\_ \_ \_ \_ Вызывающий блок верхнего уровня AC**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="19d1f-121"><dt>**PST\_AC\_TOP\_LEVEL\_CALLER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="19d1f-122">Вызывающий объект верхнего уровня должен пройти проверку, но могут существовать промежуточные библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="19d1f-122">The top-level caller must pass the check, but there may be intermediate DLLs.</span></span> <span data-ttu-id="19d1f-123">Указанный образ не обязательно является непосредственным вызывающим объектом и является приложением (. exe).</span><span class="sxs-lookup"><span data-stu-id="19d1f-123">The specified image is not necessarily the immediate caller, and is an application (.exe).</span></span><br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <span data-ttu-id="19d1f-124">PST-файл <dt>**\_ \_Непосредственный \_ вызывающий оператор AC**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="19d1f-124"><dt>**PST\_AC\_IMMEDIATE\_CALLER**</dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="19d1f-125">Прямой вызывающий объект должен пройти проверку, но не должен быть процессом верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="19d1f-125">The immediate caller must pass the check, but need not be the top-level process.</span></span> <span data-ttu-id="19d1f-126">Указанный образ является непосредственным вызывающим объектом, а образ может быть приложением (exe) или DLL.</span><span class="sxs-lookup"><span data-stu-id="19d1f-126">The specified image is the immediate caller, and the image can be an application (.exe) or a DLL.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="19d1f-127">**сзрутка**</span><span class="sxs-lookup"><span data-stu-id="19d1f-127">**szRootCA**</span></span>
</dt> <dd>

<span data-ttu-id="19d1f-128">Указатель на строку расширенных символов, представляющую корневой центр сертификации (ЦС) для сертификата; Используйте **значение NULL** для использования любого доступного ЦС.</span><span class="sxs-lookup"><span data-stu-id="19d1f-128">A pointer to a wide character string that represents the root certification authority (CA) for the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="19d1f-129">**сзиссуер**</span><span class="sxs-lookup"><span data-stu-id="19d1f-129">**szIssuer**</span></span>
</dt> <dd>

<span data-ttu-id="19d1f-130">Указатель на строку расширенных символов, которая представляет ЦС, выдавший сертификат; Используйте **значение NULL** для использования любого доступного ЦС.</span><span class="sxs-lookup"><span data-stu-id="19d1f-130">A pointer to a wide character string that represents the CA that issued the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="19d1f-131">**сзпублишер**</span><span class="sxs-lookup"><span data-stu-id="19d1f-131">**szPublisher**</span></span>
</dt> <dd>

<span data-ttu-id="19d1f-132">Указатель на строку расширенных символов, представляющую издателя программного обеспечения; Используйте **значение NULL** для использования любого доступного ЦС.</span><span class="sxs-lookup"><span data-stu-id="19d1f-132">A pointer to a wide character string that represents the software publisher; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="19d1f-133">**сзпрограмнаме**</span><span class="sxs-lookup"><span data-stu-id="19d1f-133">**szProgramName**</span></span>
</dt> <dd>

<span data-ttu-id="19d1f-134">Указатель на строку расширенных символов, представляющую имя программы; Используйте **значение NULL** для использования любого доступного ЦС.</span><span class="sxs-lookup"><span data-stu-id="19d1f-134">A pointer to a wide character string that represents the program name; use **NULL** to use any available CA.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19d1f-135">Требования</span><span class="sxs-lookup"><span data-stu-id="19d1f-135">Requirements</span></span>



| <span data-ttu-id="19d1f-136">Требование</span><span class="sxs-lookup"><span data-stu-id="19d1f-136">Requirement</span></span> | <span data-ttu-id="19d1f-137">Значение</span><span class="sxs-lookup"><span data-stu-id="19d1f-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="19d1f-138">Header</span><span class="sxs-lookup"><span data-stu-id="19d1f-138">Header</span></span><br/> | <dl> <span data-ttu-id="19d1f-139"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="19d1f-139"><dt>Pstore.h</dt></span></span> </dl> |



 

 
