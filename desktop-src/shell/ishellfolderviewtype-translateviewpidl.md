---
description: Восстанавливает указатель на список идентификаторов элементов (ПИДЛ) из одного иерархического представления папки оболочки в другое представление.
title: 'Метод Ишеллфолдервиевтипе:: Транслатевиевпидл'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 537a77e7ffffb462e0031ea0959f60cd695f7d99
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842675"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a><span data-ttu-id="85792-103">Метод Ишеллфолдервиевтипе:: Транслатевиевпидл</span><span class="sxs-lookup"><span data-stu-id="85792-103">IShellFolderViewType::TranslateViewPidl method</span></span>

<span data-ttu-id="85792-104">Восстанавливает указатель на список идентификаторов элементов (ПИДЛ) из одного иерархического представления папки оболочки в другое представление.</span><span class="sxs-lookup"><span data-stu-id="85792-104">Reconstructs a pointer to an item identifier list (PIDL) from one hierarchical representation of the Shell folder into a different representation.</span></span>

## <a name="syntax"></a><span data-ttu-id="85792-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85792-105">Syntax</span></span>


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="85792-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85792-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85792-107">*Пидл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85792-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85792-108">Тип: **пкуидлист \_ относительный**</span><span class="sxs-lookup"><span data-stu-id="85792-108">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="85792-109">Массив идентификаторов элементов относительно корневой папки.</span><span class="sxs-lookup"><span data-stu-id="85792-109">The array of item IDs relative to the root folder.</span></span>

</dd> <dt>

<span data-ttu-id="85792-110">*пидлвиев* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85792-110">*pidlView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85792-111">Тип: **пкуидлист \_ относительный**</span><span class="sxs-lookup"><span data-stu-id="85792-111">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="85792-112">Специальная ПИДЛ представления.</span><span class="sxs-lookup"><span data-stu-id="85792-112">Special PIDL of the view.</span></span>

</dd> <dt>

<span data-ttu-id="85792-113">*ппидлаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85792-113">*ppidlOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85792-114">Тип: **пкуидлист \_ Относительный \***</span><span class="sxs-lookup"><span data-stu-id="85792-114">Type: **PCUIDLIST\_RELATIVE\***</span></span>

<span data-ttu-id="85792-115">Адрес переменной ПИДЛ для получения перевода.</span><span class="sxs-lookup"><span data-stu-id="85792-115">The address of a PIDL variable to receive the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85792-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85792-116">Return value</span></span>

<span data-ttu-id="85792-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="85792-117">Type: **HRESULT**</span></span>

<span data-ttu-id="85792-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="85792-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85792-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85792-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85792-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="85792-120">Remarks</span></span>

<span data-ttu-id="85792-121">По завершении необходимо освободить возвращенный ПИДЛ с [**илфри**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span><span class="sxs-lookup"><span data-stu-id="85792-121">When finished, you should free the returned PIDL with [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="85792-122">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="85792-122">Requirements</span></span>



| <span data-ttu-id="85792-123">Требование</span><span class="sxs-lookup"><span data-stu-id="85792-123">Requirement</span></span> | <span data-ttu-id="85792-124">Значение</span><span class="sxs-lookup"><span data-stu-id="85792-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85792-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85792-125">Minimum supported client</span></span><br/> | <span data-ttu-id="85792-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="85792-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="85792-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85792-127">Minimum supported server</span></span><br/> | <span data-ttu-id="85792-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="85792-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="85792-129">DLL</span><span class="sxs-lookup"><span data-stu-id="85792-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85792-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85792-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




