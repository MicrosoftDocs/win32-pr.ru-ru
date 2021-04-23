---
description: Определяет данные ресурса.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: Структура D3DXF_FILELOADRESOURCE (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694155"
---
# <a name="d3dxf_fileloadresource-structure"></a><span data-ttu-id="9cece-103">\_Структура ФИЛЕЛОАДРЕСАУРЦЕ D3DXF</span><span class="sxs-lookup"><span data-stu-id="9cece-103">D3DXF\_FILELOADRESOURCE structure</span></span>

<span data-ttu-id="9cece-104">Определяет данные ресурса.</span><span class="sxs-lookup"><span data-stu-id="9cece-104">Identifies resource data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cece-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cece-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="9cece-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9cece-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9cece-107">**хмодуле**</span><span class="sxs-lookup"><span data-stu-id="9cece-107">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="9cece-108">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9cece-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9cece-109">Маркер модуля, содержащего загружаемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="9cece-109">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="9cece-110">Если этот член имеет **значение NULL**, ресурс должен быть присоединен к исполняемому файлу, который будет его использовать.</span><span class="sxs-lookup"><span data-stu-id="9cece-110">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="9cece-111">**лпнаме**</span><span class="sxs-lookup"><span data-stu-id="9cece-111">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="9cece-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9cece-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9cece-113">Указатель на строку, указывающую имя загружаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="9cece-113">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="9cece-114">Например, если ресурс является сеткой, этот член должен указать имя файла сетки.</span><span class="sxs-lookup"><span data-stu-id="9cece-114">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="9cece-115">**лптипе**</span><span class="sxs-lookup"><span data-stu-id="9cece-115">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="9cece-116">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9cece-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9cece-117">Указатель на строку, указывающую определяемый пользователем тип, идентифицирующий ресурс.</span><span class="sxs-lookup"><span data-stu-id="9cece-117">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cece-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9cece-118">Remarks</span></span>

<span data-ttu-id="9cece-119">Эта структура определяет ресурс для загрузки, когда приложение использует метод [**креатинумобжект**](id3dxfile--createenumobject.md) и задает флаг [D3DXF \_ филелоад \_ фромресаурце](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="9cece-119">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the [D3DXF\_FILELOAD\_FROMRESOURCE](d3dxf.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cece-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9cece-120">Requirements</span></span>



| <span data-ttu-id="9cece-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9cece-121">Requirement</span></span> | <span data-ttu-id="9cece-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9cece-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cece-123">Header</span><span class="sxs-lookup"><span data-stu-id="9cece-123">Header</span></span><br/> | <dl> <span data-ttu-id="9cece-124"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cece-124"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cece-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cece-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cece-126">Структуры файлов D3DX X</span><span class="sxs-lookup"><span data-stu-id="9cece-126">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
