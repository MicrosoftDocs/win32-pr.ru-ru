---
description: Указывает, что был запущен Поиск.
title: 'Метод Ишеллфолдерсеарчаблекаллбакк:: Рунбегин'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 2bef0f29486143f97f886c0d31ab456a070ed857
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543111"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a><span data-ttu-id="26557-103">Метод Ишеллфолдерсеарчаблекаллбакк:: Рунбегин</span><span class="sxs-lookup"><span data-stu-id="26557-103">IShellFolderSearchableCallback::RunBegin method</span></span>

<span data-ttu-id="26557-104">Указывает, что был запущен Поиск.</span><span class="sxs-lookup"><span data-stu-id="26557-104">Indicates that a search was started.</span></span>

## <a name="syntax"></a><span data-ttu-id="26557-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26557-105">Syntax</span></span>


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="26557-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26557-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26557-107">*двресервед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26557-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26557-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="26557-108">Type: **DWORD**</span></span>

<span data-ttu-id="26557-109">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="26557-109">Reserved.</span></span> <span data-ttu-id="26557-110">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="26557-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26557-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26557-111">Return value</span></span>

<span data-ttu-id="26557-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="26557-112">Type: **HRESULT**</span></span>

<span data-ttu-id="26557-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="26557-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26557-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26557-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="26557-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="26557-115">Remarks</span></span>

<span data-ttu-id="26557-116">В ответ на этот обратный вызов приложение может включить кнопку **Отмена** , например.</span><span class="sxs-lookup"><span data-stu-id="26557-116">In response to this callback, the application may enable the **Cancel** button, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="26557-117">Требования</span><span class="sxs-lookup"><span data-stu-id="26557-117">Requirements</span></span>



| <span data-ttu-id="26557-118">Требование</span><span class="sxs-lookup"><span data-stu-id="26557-118">Requirement</span></span> | <span data-ttu-id="26557-119">Значение</span><span class="sxs-lookup"><span data-stu-id="26557-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26557-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26557-120">Minimum supported client</span></span><br/> | <span data-ttu-id="26557-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26557-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="26557-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26557-122">Minimum supported server</span></span><br/> | <span data-ttu-id="26557-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26557-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="26557-124">DLL</span><span class="sxs-lookup"><span data-stu-id="26557-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26557-125"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26557-125"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




