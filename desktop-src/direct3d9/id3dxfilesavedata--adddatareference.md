---
description: Добавляет ссылку на данные в качестве дочернего элемента для этого узла данных ID3DXFileSaveData File. Ссылка на данные указывает на объект данных файла.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'Метод ID3DXFileSaveData:: Адддатареференце (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000416"
---
# <a name="id3dxfilesavedataadddatareference-method"></a><span data-ttu-id="940a3-104">Метод ID3DXFileSaveData:: Адддатареференце</span><span class="sxs-lookup"><span data-stu-id="940a3-104">ID3DXFileSaveData::AddDataReference method</span></span>

<span data-ttu-id="940a3-105">Добавляет ссылку на данные в качестве дочернего элемента для этого узла данных [**ID3DXFileSaveData**](id3dxfilesavedata.md) File.</span><span class="sxs-lookup"><span data-stu-id="940a3-105">Adds a data reference as a child of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span> <span data-ttu-id="940a3-106">Ссылка на данные указывает на объект данных файла.</span><span class="sxs-lookup"><span data-stu-id="940a3-106">The data reference points to a file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="940a3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="940a3-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a><span data-ttu-id="940a3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="940a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="940a3-109">*szName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="940a3-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940a3-110">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="940a3-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="940a3-111">Указатель на имя объекта данных, который необходимо добавить по ссылке.</span><span class="sxs-lookup"><span data-stu-id="940a3-111">Pointer to the name of the data object to add by reference.</span></span> <span data-ttu-id="940a3-112">Укажите **значение NULL** , если у объекта данных нет имени.</span><span class="sxs-lookup"><span data-stu-id="940a3-112">Specify **NULL** if the data object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="940a3-113">*идентификатор процесса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="940a3-113">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940a3-114">Тип: **константа [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="940a3-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="940a3-115">Указатель на идентификатор GUID, представляющий объект данных, который необходимо добавить по ссылке.</span><span class="sxs-lookup"><span data-stu-id="940a3-115">Pointer to a GUID representing the data object to add by reference.</span></span> <span data-ttu-id="940a3-116">Если **значение равно NULL**, будет добавлена ссылка, указывающая на объект данных с именем, заданным параметром szName.</span><span class="sxs-lookup"><span data-stu-id="940a3-116">If **NULL**, a reference will be added that points to the data object with the name given by szName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="940a3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="940a3-117">Return value</span></span>

<span data-ttu-id="940a3-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="940a3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="940a3-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="940a3-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="940a3-120">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадобжект, D3DXFERR \_ Бадвалуе, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="940a3-120">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="940a3-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="940a3-121">Remarks</span></span>

<span data-ttu-id="940a3-122">Объект данных файла, на который указывает ссылка, должен иметь либо имя, либо идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="940a3-122">The file data object being referenced must have either a name or a GUID.</span></span> <span data-ttu-id="940a3-123">Объект данных файла также должен быть производным от другого родительского объекта [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="940a3-123">The file data object must also derive from a different parent [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="940a3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="940a3-124">Requirements</span></span>



| <span data-ttu-id="940a3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="940a3-125">Requirement</span></span> | <span data-ttu-id="940a3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="940a3-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="940a3-127">Header</span><span class="sxs-lookup"><span data-stu-id="940a3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="940a3-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="940a3-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="940a3-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="940a3-129">Library</span></span><br/> | <dl> <span data-ttu-id="940a3-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="940a3-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="940a3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="940a3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940a3-132">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="940a3-132">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
