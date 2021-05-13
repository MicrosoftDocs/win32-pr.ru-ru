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
ms.openlocfilehash: 1627bb134066821444788ca44a3527278a02f4c7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842775"
---
# <a name="ishellfolderviewtypeenumviews-method"></a><span data-ttu-id="b8355-103">Метод Ишеллфолдервиевтипе:: Енумвиевс</span><span class="sxs-lookup"><span data-stu-id="b8355-103">IShellFolderViewType::EnumViews method</span></span>

<span data-ttu-id="b8355-104">Извлекает перечислитель, возвращающий один указатель на список идентификаторов элементов (ПИДЛ) для каждого расширенного представления.</span><span class="sxs-lookup"><span data-stu-id="b8355-104">Retrieves an enumerator that will return one pointer to an item identifier list (PIDL) for every extended view.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8355-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8355-105">Syntax</span></span>


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="b8355-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8355-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8355-107">*грффлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8355-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8355-108">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="b8355-108">Type: **ULONG**</span></span>

<span data-ttu-id="b8355-109">Флаги, указывающие, какие элементы следует включить в перечисление.</span><span class="sxs-lookup"><span data-stu-id="b8355-109">Flags indicating which items to include in the enumeration.</span></span> <span data-ttu-id="b8355-110">Список возможных значений см. в разделе перечислимый тип [**шконтф**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) .</span><span class="sxs-lookup"><span data-stu-id="b8355-110">For a list of possible values, see the [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) enumerated type.</span></span> <span data-ttu-id="b8355-111">Этот параметр можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="b8355-111">This parameter may be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b8355-112">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b8355-112">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8355-113">Тип: **[ **иенумидлист**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span><span class="sxs-lookup"><span data-stu-id="b8355-113">Type: **[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span></span>

<span data-ttu-id="b8355-114">Адрес переменной-указателя типа [**иенумидлист**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) , которая получает перечислитель.</span><span class="sxs-lookup"><span data-stu-id="b8355-114">The address of a pointer variable of type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) that receives the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8355-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8355-115">Return value</span></span>

<span data-ttu-id="b8355-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b8355-116">Type: **HRESULT**</span></span>

<span data-ttu-id="b8355-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b8355-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b8355-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b8355-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8355-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="b8355-119">Remarks</span></span>

<span data-ttu-id="b8355-120">Представления представлены пользователю в виде скрытых папок из корневого каталога (представленного PIDL).</span><span class="sxs-lookup"><span data-stu-id="b8355-120">Views are represented to the user as hidden folders off the root directory (represented by PIDLs).</span></span> <span data-ttu-id="b8355-121">При необходимости представление по умолчанию (в корневой папке) представляется как null или пустое **значение** Пидл.</span><span class="sxs-lookup"><span data-stu-id="b8355-121">Whenever appropriate, the default view (off the root folder) is represented as the **NULL**, or empty, PIDL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8355-122">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="b8355-122">Requirements</span></span>



| <span data-ttu-id="b8355-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b8355-123">Requirement</span></span> | <span data-ttu-id="b8355-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b8355-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8355-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8355-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b8355-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8355-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b8355-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8355-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b8355-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8355-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b8355-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b8355-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8355-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8355-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




