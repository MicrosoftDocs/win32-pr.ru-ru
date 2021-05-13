---
description: Делает этот указатель на список идентификаторов элементов (ПИДЛ) недопустимой частью папки оболочки.
title: 'Метод Ишеллфолдерсеарчабле:: Инвалидатесеарч'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 43d76c6a27b301a61474b8028af16e5e540cf2ce
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841695"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a><span data-ttu-id="34691-103">Метод Ишеллфолдерсеарчабле:: Инвалидатесеарч</span><span class="sxs-lookup"><span data-stu-id="34691-103">IShellFolderSearchable::InvalidateSearch method</span></span>

<span data-ttu-id="34691-104">Делает этот указатель на список идентификаторов элементов (ПИДЛ) недопустимой частью папки оболочки.</span><span class="sxs-lookup"><span data-stu-id="34691-104">Makes this pointer to an item identifier list (PIDL) an invalid portion of the Shell folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="34691-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34691-105">Syntax</span></span>


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="34691-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="34691-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34691-107">*пидлсеарч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34691-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34691-108">Тип: **лпЦитемидлист**</span><span class="sxs-lookup"><span data-stu-id="34691-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="34691-109">Указатель на структуру [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) для папки поиска.</span><span class="sxs-lookup"><span data-stu-id="34691-109">A pointer to the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> <dt>

<span data-ttu-id="34691-110">*пдвфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34691-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34691-111">Тип: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="34691-111">Type: **DWORD\***</span></span>

<span data-ttu-id="34691-112">Флаги в настоящее время не определены; Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="34691-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34691-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34691-113">Return value</span></span>

<span data-ttu-id="34691-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="34691-114">Type: **HRESULT**</span></span>

<span data-ttu-id="34691-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="34691-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="34691-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="34691-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="34691-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="34691-117">Remarks</span></span>

<span data-ttu-id="34691-118">Если папка поиска становится недействительной, она может выполнить очистку всех используемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34691-118">When a search folder is invalidated, it can perform cleanup of any resources it has used.</span></span> <span data-ttu-id="34691-119">Метод **ишеллфолдерсеарчабле:: инвалидатесеарч** может привести к отмене асинхронного поиска и приведет к выходу окончательного выпуска объекта интерфейса [**ишеллфолдерсеарчаблекаллбакк**](ishellfoldersearchablecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="34691-119">The **IShellFolderSearchable::InvalidateSearch** method may cause an asynchronous search to be canceled and will result in the eventual release of the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface object.</span></span>

## <a name="requirements"></a><span data-ttu-id="34691-120">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="34691-120">Requirements</span></span>



| <span data-ttu-id="34691-121">Требование</span><span class="sxs-lookup"><span data-stu-id="34691-121">Requirement</span></span> | <span data-ttu-id="34691-122">Значение</span><span class="sxs-lookup"><span data-stu-id="34691-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34691-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34691-123">Minimum supported client</span></span><br/> | <span data-ttu-id="34691-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34691-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="34691-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34691-125">Minimum supported server</span></span><br/> | <span data-ttu-id="34691-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34691-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="34691-127">DLL</span><span class="sxs-lookup"><span data-stu-id="34691-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34691-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34691-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




