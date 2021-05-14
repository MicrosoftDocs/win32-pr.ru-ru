---
description: Возвращает имя представления по умолчанию. Вызовите Жетдисплайнамеоф, чтобы получить имена других представлений.
title: 'Метод Ишеллфолдервиевтипе:: Жетдефаултвиевнаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 808f68093512e2da602d5e73775b47943b140a46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842765"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="22783-104">Метод Ишеллфолдервиевтипе:: Жетдефаултвиевнаме</span><span class="sxs-lookup"><span data-stu-id="22783-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="22783-105">Возвращает имя представления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22783-105">Gets the name of the default view.</span></span> <span data-ttu-id="22783-106">Вызовите [**жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) , чтобы получить имена других представлений.</span><span class="sxs-lookup"><span data-stu-id="22783-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="22783-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22783-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="22783-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="22783-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22783-109">*уфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22783-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22783-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="22783-110">Type: **DWORD**</span></span>

<span data-ttu-id="22783-111">Необязательные флаги; необходимо задать значение 0.</span><span class="sxs-lookup"><span data-stu-id="22783-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="22783-112">*ппвсзнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="22783-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22783-113">Тип: **LPWSTR \***</span><span class="sxs-lookup"><span data-stu-id="22783-113">Type: **LPWSTR\***</span></span>

<span data-ttu-id="22783-114">Адрес указателя строки, который получает имя представления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22783-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="22783-115">Память для строки выделяется с помощью [**шстрдуп**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span><span class="sxs-lookup"><span data-stu-id="22783-115">The memory for the string is allocated with [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22783-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22783-116">Return value</span></span>

<span data-ttu-id="22783-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="22783-117">Type: **HRESULT**</span></span>

<span data-ttu-id="22783-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="22783-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22783-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22783-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="22783-120">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="22783-120">Requirements</span></span>



| <span data-ttu-id="22783-121">Требование</span><span class="sxs-lookup"><span data-stu-id="22783-121">Requirement</span></span> | <span data-ttu-id="22783-122">Значение</span><span class="sxs-lookup"><span data-stu-id="22783-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22783-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22783-123">Minimum supported client</span></span><br/> | <span data-ttu-id="22783-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22783-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="22783-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22783-125">Minimum supported server</span></span><br/> | <span data-ttu-id="22783-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22783-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="22783-127">DLL</span><span class="sxs-lookup"><span data-stu-id="22783-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22783-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22783-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




