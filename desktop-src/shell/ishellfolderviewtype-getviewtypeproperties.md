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
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984624"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="0ab16-103">Метод Ишеллфолдервиевтипе:: Жетвиевтипепропертиес</span><span class="sxs-lookup"><span data-stu-id="0ab16-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="0ab16-104">Возвращает свойства представления.</span><span class="sxs-lookup"><span data-stu-id="0ab16-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ab16-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ab16-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0ab16-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ab16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ab16-107">*Пидл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ab16-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab16-108">Тип: **\_ дочерний элемент пкуитемид**</span><span class="sxs-lookup"><span data-stu-id="0ab16-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="0ab16-109">ПИДЛ.</span><span class="sxs-lookup"><span data-stu-id="0ab16-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="0ab16-110">*пдвфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0ab16-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab16-111">Введите: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="0ab16-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="0ab16-112">Указатель на целочисленную переменную без знака, которая получает свойства представления, которые указывают действия, выполняемые при выборе представления.</span><span class="sxs-lookup"><span data-stu-id="0ab16-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="0ab16-113">Флагами могут быть любые сочетания следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0ab16-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="0ab16-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *Сфвтфлаг \_ уведомлять \_ CREATE*\* (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="0ab16-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG\_NOTIFY\_CREATE*\* (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="0ab16-115">Создать элемент представления, если нет.</span><span class="sxs-lookup"><span data-stu-id="0ab16-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="0ab16-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**Сфвтфлаг \_ УВЕДОМЛЕНИЕ \_ курорт** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="0ab16-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="0ab16-117">Повторно вставьте ПИДЛ и повторите сортировку.</span><span class="sxs-lookup"><span data-stu-id="0ab16-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ab16-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ab16-118">Return value</span></span>

<span data-ttu-id="0ab16-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0ab16-119">Type: **HRESULT**</span></span>

<span data-ttu-id="0ab16-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0ab16-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0ab16-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ab16-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ab16-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0ab16-122">Requirements</span></span>



| <span data-ttu-id="0ab16-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0ab16-123">Requirement</span></span> | <span data-ttu-id="0ab16-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0ab16-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab16-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ab16-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0ab16-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0ab16-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0ab16-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ab16-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0ab16-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0ab16-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0ab16-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0ab16-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ab16-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ab16-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




