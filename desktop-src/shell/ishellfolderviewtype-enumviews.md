---
description: Извлекает перечислитель, возвращающий один указатель на список идентификаторов элементов (ПИДЛ) для каждого расширенного представления.
title: 'Метод Ишеллфолдервиевтипе:: Енумвиевс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 4ccaac7baf99608e097b8f8b67c8eac30f60ed3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997279"
---
# <a name="ishellfolderviewtypeenumviews-method"></a><span data-ttu-id="ce950-103">Метод Ишеллфолдервиевтипе:: Енумвиевс</span><span class="sxs-lookup"><span data-stu-id="ce950-103">IShellFolderViewType::EnumViews method</span></span>

<span data-ttu-id="ce950-104">Извлекает перечислитель, возвращающий один указатель на список идентификаторов элементов (ПИДЛ) для каждого расширенного представления.</span><span class="sxs-lookup"><span data-stu-id="ce950-104">Retrieves an enumerator that will return one pointer to an item identifier list (PIDL) for every extended view.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce950-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce950-105">Syntax</span></span>


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="ce950-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce950-107">*грффлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce950-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce950-108">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="ce950-108">Type: **ULONG**</span></span>

<span data-ttu-id="ce950-109">Флаги, указывающие, какие элементы следует включить в перечисление.</span><span class="sxs-lookup"><span data-stu-id="ce950-109">Flags indicating which items to include in the enumeration.</span></span> <span data-ttu-id="ce950-110">Список возможных значений см. в разделе перечислимый тип [**шконтф**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) .</span><span class="sxs-lookup"><span data-stu-id="ce950-110">For a list of possible values, see the [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) enumerated type.</span></span> <span data-ttu-id="ce950-111">Этот параметр можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="ce950-111">This parameter may be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="ce950-112">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ce950-112">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce950-113">Тип: **[ **иенумидлист**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span><span class="sxs-lookup"><span data-stu-id="ce950-113">Type: **[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span></span>

<span data-ttu-id="ce950-114">Адрес переменной-указателя типа [**иенумидлист**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) , которая получает перечислитель.</span><span class="sxs-lookup"><span data-stu-id="ce950-114">The address of a pointer variable of type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) that receives the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce950-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce950-115">Return value</span></span>

<span data-ttu-id="ce950-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ce950-116">Type: **HRESULT**</span></span>

<span data-ttu-id="ce950-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ce950-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce950-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce950-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce950-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce950-119">Remarks</span></span>

<span data-ttu-id="ce950-120">Представления представлены пользователю в виде скрытых папок из корневого каталога (представленного PIDL).</span><span class="sxs-lookup"><span data-stu-id="ce950-120">Views are represented to the user as hidden folders off the root directory (represented by PIDLs).</span></span> <span data-ttu-id="ce950-121">При необходимости представление по умолчанию (в корневой папке) представляется как null или пустое **значение** Пидл.</span><span class="sxs-lookup"><span data-stu-id="ce950-121">Whenever appropriate, the default view (off the root folder) is represented as the **NULL**, or empty, PIDL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce950-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ce950-122">Requirements</span></span>



| <span data-ttu-id="ce950-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ce950-123">Requirement</span></span> | <span data-ttu-id="ce950-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ce950-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce950-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce950-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ce950-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce950-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ce950-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce950-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ce950-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce950-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ce950-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ce950-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce950-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce950-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




