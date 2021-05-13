---
description: Указывает, что Поиск завершен.
title: 'Метод Ишеллфолдерсеарчаблекаллбакк:: Руненд'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunEnd
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91700764-6cdf-488d-adc0-e34d9b4cb71d
ms.openlocfilehash: c23d461fdbd175a80a8fa94fcc238f6cf2f89869
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842825"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="6c62d-103">Метод Ишеллфолдерсеарчаблекаллбакк:: Руненд</span><span class="sxs-lookup"><span data-stu-id="6c62d-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="6c62d-104">Указывает, что Поиск завершен.</span><span class="sxs-lookup"><span data-stu-id="6c62d-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c62d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c62d-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="6c62d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c62d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c62d-107">*двресервед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c62d-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c62d-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6c62d-108">Type: **DWORD**</span></span>

<span data-ttu-id="6c62d-109">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="6c62d-109">Reserved.</span></span> <span data-ttu-id="6c62d-110">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="6c62d-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c62d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c62d-111">Return value</span></span>

<span data-ttu-id="6c62d-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6c62d-112">Type: **HRESULT**</span></span>

<span data-ttu-id="6c62d-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6c62d-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c62d-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6c62d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c62d-115">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="6c62d-115">Requirements</span></span>



| <span data-ttu-id="6c62d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6c62d-116">Requirement</span></span> | <span data-ttu-id="6c62d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6c62d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c62d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c62d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6c62d-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c62d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6c62d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c62d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6c62d-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c62d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6c62d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6c62d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c62d-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c62d-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




