---
description: Вызывает библиотеку, чтобы получить состояние безопасности относительно узла и использовать скрипт или MSI.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Функция Влдпжетлоккдовнполици (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538750"
---
# <a name="wldpgetlockdownpolicy-function"></a><span data-ttu-id="21dd1-103">Функция Влдпжетлоккдовнполици</span><span class="sxs-lookup"><span data-stu-id="21dd1-103">WldpGetLockdownPolicy function</span></span>

<span data-ttu-id="21dd1-104">Вызывает библиотеку, чтобы получить состояние безопасности относительно узла и использовать скрипт или MSI.</span><span class="sxs-lookup"><span data-stu-id="21dd1-104">Calls the library to get the security state relative to the host, and script or msi to be used.</span></span> <span data-ttu-id="21dd1-105">У функции нет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="21dd1-105">The function has no associated import library.</span></span> <span data-ttu-id="21dd1-106">Для динамической привязки к wldp.dll необходимо использовать функции LoadLibrary и GetProcAddress.</span><span class="sxs-lookup"><span data-stu-id="21dd1-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="21dd1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21dd1-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a><span data-ttu-id="21dd1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="21dd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21dd1-109">*хостинформатион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="21dd1-109">*hostInformation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="21dd1-110">Структура [**\_ \_ информации узла WLDP**](wldp-host-information.md) , определяющая узел и исходный файл для оценки.</span><span class="sxs-lookup"><span data-stu-id="21dd1-110">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host and source file to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="21dd1-111">*локкдовнстате* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="21dd1-111">*lockdownState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21dd1-112">Предоставляет результирующее значение безопасной политики.</span><span class="sxs-lookup"><span data-stu-id="21dd1-112">Provides the resulting policy secure value.</span></span> <span data-ttu-id="21dd1-113">Наличии! WLDP_LOCKDOWN_IS_OFF, то УМЦИ включен.</span><span class="sxs-lookup"><span data-stu-id="21dd1-113">If !WLDP_LOCKDOWN_IS_OFF, then UMCI is enabled.</span></span> <span data-ttu-id="21dd1-114">Можно также проверить WLDP_LOCKDOWN_IS_AUDIT и WLDP_LOCKDOWN_IS_ENFORCE, чтобы определить, находится ли политика в режиме аудита или принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="21dd1-114">You can also check WLDP_LOCKDOWN_IS_AUDIT and WLDP_LOCKDOWN_IS_ENFORCE to determine if a policy is in audit or enforce mode.</span></span>
</dd> <dt>

<span data-ttu-id="21dd1-115">*локкдовнфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21dd1-115">*lockdownFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21dd1-116">Следующие значения флагов определены WLDP \_ flags \_ скипсигнатуревалидатион 0x00000100 — Если задано значение, пропускать проверку SaferIdentifyLevel, которая будет пропускать, подписан ли сценарий.</span><span class="sxs-lookup"><span data-stu-id="21dd1-116">The following flag values are defined WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION 0x00000100 – when set, skip the SaferIdentifyLevel validation, which will ignore whether a script is signed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21dd1-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21dd1-117">Return value</span></span>

<span data-ttu-id="21dd1-118">Этот метод возвращает \_ значение ОК в случае успеха или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="21dd1-118">This method returns S\_OK if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="21dd1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21dd1-119">Remarks</span></span>

<span data-ttu-id="21dd1-120">При вызове со \_ \_ сведениями об узле WLDP. СЗСАУРЦЕ = NULL возвращается универсальная политика для узла.</span><span class="sxs-lookup"><span data-stu-id="21dd1-120">When called with WLDP\_HOST\_INFORMATION.szSource = NULL, the generic policy for the host is returned.</span></span>

<span data-ttu-id="21dd1-121">При вызове со \_ \_ сведениями об узле WLDP. ДВХОСТИД = WLDP \_ \_ идентификатор узла \_ Global, WLDP \_ \_ сведения об узле. сзсаурце должен иметь значение null, а функция вернет глобальную системную политику.</span><span class="sxs-lookup"><span data-stu-id="21dd1-121">When called with WLDP\_HOST\_INFORMATION.dwHostId = WLDP\_HOST\_ID\_GLOBAL, WLDP\_HOST\_INFORMATION.szSource must be NULL, and the function will return the global system policy.</span></span>

<span data-ttu-id="21dd1-122">DwFlag WLDP \_ flags \_ скипсигнатуревалидатион можно использовать для пропуска проверки SaferIdentifyLevel (), которая будет пропускать, подписан ли скрипт.</span><span class="sxs-lookup"><span data-stu-id="21dd1-122">The dwFlag WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION can be used to skip the SaferIdentifyLevel() validation, which will ignore whether a script is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="21dd1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="21dd1-123">Requirements</span></span>



| <span data-ttu-id="21dd1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="21dd1-124">Requirement</span></span> | <span data-ttu-id="21dd1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="21dd1-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="21dd1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21dd1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="21dd1-127">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="21dd1-127">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="21dd1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21dd1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="21dd1-129">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="21dd1-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="21dd1-130">Header</span><span class="sxs-lookup"><span data-stu-id="21dd1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="21dd1-131"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="21dd1-131"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="21dd1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="21dd1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21dd1-133"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21dd1-133"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




