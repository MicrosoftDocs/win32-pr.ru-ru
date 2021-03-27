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
ms.openlocfilehash: 73155e65f4b6edb4a4b4b9b0d52ab5b042fa68b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997443"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="3b425-103">Метод Ишеллфолдерсеарчаблекаллбакк:: Руненд</span><span class="sxs-lookup"><span data-stu-id="3b425-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="3b425-104">Указывает, что Поиск завершен.</span><span class="sxs-lookup"><span data-stu-id="3b425-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b425-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b425-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="3b425-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b425-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b425-107">*двресервед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3b425-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b425-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3b425-108">Type: **DWORD**</span></span>

<span data-ttu-id="3b425-109">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3b425-109">Reserved.</span></span> <span data-ttu-id="3b425-110">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="3b425-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b425-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b425-111">Return value</span></span>

<span data-ttu-id="3b425-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3b425-112">Type: **HRESULT**</span></span>

<span data-ttu-id="3b425-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3b425-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b425-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b425-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b425-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3b425-115">Requirements</span></span>



| <span data-ttu-id="3b425-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3b425-116">Requirement</span></span> | <span data-ttu-id="3b425-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3b425-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b425-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b425-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3b425-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b425-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3b425-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b425-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3b425-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b425-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3b425-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3b425-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b425-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b425-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




