---
description: Обратный вызов, позволяющий пользователю зарегистрировать шаблон файла. x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'Метод ID3DXSaveUserData:: Регистертемплатес (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1465b76b758f6a5ed9e7dff4c7126935fb7c5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713959"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a><span data-ttu-id="61a1e-103">Метод ID3DXSaveUserData:: Регистертемплатес</span><span class="sxs-lookup"><span data-stu-id="61a1e-103">ID3DXSaveUserData::RegisterTemplates method</span></span>

<span data-ttu-id="61a1e-104">Обратный вызов, позволяющий пользователю зарегистрировать шаблон файла. x.</span><span class="sxs-lookup"><span data-stu-id="61a1e-104">A callback for the user to register a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a1e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61a1e-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a><span data-ttu-id="61a1e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="61a1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a1e-107">*пксфилеапи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="61a1e-107">*pXFileApi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61a1e-108">Тип: **[ **LPD3DXFILE**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="61a1e-108">Type: **[**LPD3DXFILE**](id3dxfile.md)**</span></span>

<span data-ttu-id="61a1e-109">Этот указатель используется для регистрации определяемых пользователем шаблонов файлов x.</span><span class="sxs-lookup"><span data-stu-id="61a1e-109">Use this pointer to register user-defined .x file templates.</span></span> <span data-ttu-id="61a1e-110">См. [**ID3DXFile**](id3dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="61a1e-110">See [**ID3DXFile**](id3dxfile.md).</span></span> <span data-ttu-id="61a1e-111">Не используйте этот параметр для добавления объектов данных.</span><span class="sxs-lookup"><span data-stu-id="61a1e-111">Do not use this parameter to add data objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61a1e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61a1e-112">Return value</span></span>

<span data-ttu-id="61a1e-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="61a1e-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="61a1e-114">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="61a1e-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="61a1e-115">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="61a1e-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="61a1e-116">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md), так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="61a1e-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="61a1e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61a1e-117">Remarks</span></span>

<span data-ttu-id="61a1e-118">**ID3DXSaveUserData:: регистертемплатес** и [**ID3DXSaveUserData:: саветемплатес**](id3dxsaveuserdata--savetemplates.md) предоставляют механизм для добавления шаблона в файл. x для сохранения пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="61a1e-118">**ID3DXSaveUserData::RegisterTemplates** and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="61a1e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="61a1e-119">Requirements</span></span>



| <span data-ttu-id="61a1e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="61a1e-120">Requirement</span></span> | <span data-ttu-id="61a1e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="61a1e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61a1e-122">Header</span><span class="sxs-lookup"><span data-stu-id="61a1e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="61a1e-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="61a1e-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="61a1e-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="61a1e-124">Library</span></span><br/> | <dl> <span data-ttu-id="61a1e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61a1e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="61a1e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61a1e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a1e-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="61a1e-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
