---
description: Проверяет, что профиль пользователя в сети загружен.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Функция Онпрофилелоадед (Лсаидпров. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813601"
---
# <a name="onprofileloaded-function"></a><span data-ttu-id="f8659-103">Функция Онпрофилелоадед</span><span class="sxs-lookup"><span data-stu-id="f8659-103">OnProfileLoaded function</span></span>

<span data-ttu-id="f8659-104">Проверяет, что профиль пользователя в сети загружен.</span><span class="sxs-lookup"><span data-stu-id="f8659-104">Checks that the online user profile is loaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8659-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8659-105">Syntax</span></span>


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a><span data-ttu-id="f8659-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8659-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8659-107">*Провидерхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8659-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8659-108">Обработчик поставщика.</span><span class="sxs-lookup"><span data-stu-id="f8659-108">The provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="f8659-109">*UserToken* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8659-109">*UserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8659-110">Токен пользователя, профиль которого загружается или выгружается.</span><span class="sxs-lookup"><span data-stu-id="f8659-110">Token of the user whose profile is being loaded or unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="f8659-111">*Загружено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8659-111">*Loaded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8659-112">**Значение true** , если профиль загружен.</span><span class="sxs-lookup"><span data-stu-id="f8659-112">**TRUE** if the profile has been loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8659-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8659-113">Return value</span></span>

<span data-ttu-id="f8659-114">Если функция завершается успешно, функция возвращает состояние \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f8659-114">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="f8659-115">Если функция завершается с ошибкой, функция возвращает ненулевой код ошибки, который является специфической для поставщика ошибкой в целях диагностики.</span><span class="sxs-lookup"><span data-stu-id="f8659-115">If the function fails, the function returns a nonzero error code that is a provider-specific error for diagnostic purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8659-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8659-116">Remarks</span></span>

<span data-ttu-id="f8659-117">Эта функция вызывается каждый раз при вызове функции [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="f8659-117">This function is called each time the [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) function is called.</span></span> <span data-ttu-id="f8659-118">Он не синхронизирован с **LoadUserProfile**; Это значит, что **LoadUserProfile** мог вернуть, а профиль мог быть выгружен на момент вызова функции.</span><span class="sxs-lookup"><span data-stu-id="f8659-118">It is not synchronized with **LoadUserProfile**; that is, **LoadUserProfile** might have returned and the profile might have been unloaded by the time the function was called.</span></span> <span data-ttu-id="f8659-119">Эта функция может вызываться несколько раз даже после загрузки профиля.</span><span class="sxs-lookup"><span data-stu-id="f8659-119">This function can be called more than once even when the profile has been loaded.</span></span> <span data-ttu-id="f8659-120">Поставщик удостоверений не должен рассчитывать на то, что вызов этой функции с *загрузкой* , РАВНым true, должен сопровождаться вызовом с параметром *Loaded* , равным false.</span><span class="sxs-lookup"><span data-stu-id="f8659-120">The identity provider must not assume that a call to this function with *Loaded* equal to TRUE will be followed by a call with *Loaded* equal to FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8659-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f8659-121">Requirements</span></span>



| <span data-ttu-id="f8659-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f8659-122">Requirement</span></span> | <span data-ttu-id="f8659-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f8659-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8659-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8659-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f8659-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f8659-125">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f8659-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8659-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f8659-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f8659-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f8659-128">Header</span><span class="sxs-lookup"><span data-stu-id="f8659-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8659-129"><dt>Лсаидпров. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8659-129"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

 
