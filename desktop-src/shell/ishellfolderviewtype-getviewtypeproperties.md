---
description: Возвращает свойства представления.
title: 'Метод Ишеллфолдервиевтипе:: Жетвиевтипепропертиес'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f5c7c6b75c89711a69ac578b3d04a72362b1eac9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842705"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="e3ac9-103">Метод Ишеллфолдервиевтипе:: Жетвиевтипепропертиес</span><span class="sxs-lookup"><span data-stu-id="e3ac9-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="e3ac9-104">Возвращает свойства представления.</span><span class="sxs-lookup"><span data-stu-id="e3ac9-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ac9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3ac9-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e3ac9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3ac9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3ac9-107">*Пидл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3ac9-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ac9-108">Тип: **\_ дочерний элемент пкуитемид**</span><span class="sxs-lookup"><span data-stu-id="e3ac9-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="e3ac9-109">ПИДЛ.</span><span class="sxs-lookup"><span data-stu-id="e3ac9-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="e3ac9-110">*пдвфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3ac9-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ac9-111">Тип: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="e3ac9-111">Type: **DWORD\***</span></span>

<span data-ttu-id="e3ac9-112">Указатель на целочисленную переменную без знака, которая получает свойства представления, которые указывают действия, выполняемые при выборе представления.</span><span class="sxs-lookup"><span data-stu-id="e3ac9-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="e3ac9-113">Флагами могут быть любые сочетания следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e3ac9-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="e3ac9-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**Сфвтфлаг \_ УВЕДОМЛЕНИЕ о \_ создании** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="e3ac9-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG\_NOTIFY\_CREATE** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="e3ac9-115">Создать элемент представления, если нет.</span><span class="sxs-lookup"><span data-stu-id="e3ac9-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="e3ac9-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**Сфвтфлаг \_ УВЕДОМЛЕНИЕ \_ курорт** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e3ac9-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="e3ac9-117">Повторно вставьте ПИДЛ и повторите сортировку.</span><span class="sxs-lookup"><span data-stu-id="e3ac9-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3ac9-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3ac9-118">Return value</span></span>

<span data-ttu-id="e3ac9-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e3ac9-119">Type: **HRESULT**</span></span>

<span data-ttu-id="e3ac9-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e3ac9-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3ac9-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3ac9-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ac9-122">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="e3ac9-122">Requirements</span></span>



| <span data-ttu-id="e3ac9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e3ac9-123">Requirement</span></span> | <span data-ttu-id="e3ac9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e3ac9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ac9-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3ac9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ac9-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e3ac9-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e3ac9-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3ac9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ac9-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e3ac9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e3ac9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e3ac9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3ac9-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3ac9-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




