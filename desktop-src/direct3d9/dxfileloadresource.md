---
description: Определяет данные ресурса. Не рекомендуется.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Структура ДКСФИЛЕЛОАДРЕСАУРЦЕ (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 233fe6acb13a6ae654a714028a316d7d6f6871ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647861"
---
# <a name="dxfileloadresource-structure"></a><span data-ttu-id="829e4-104">Структура ДКСФИЛЕЛОАДРЕСАУРЦЕ</span><span class="sxs-lookup"><span data-stu-id="829e4-104">DXFILELOADRESOURCE structure</span></span>

<span data-ttu-id="829e4-105">Определяет данные ресурса.</span><span class="sxs-lookup"><span data-stu-id="829e4-105">Identifies resource data.</span></span> <span data-ttu-id="829e4-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="829e4-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="829e4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="829e4-107">Syntax</span></span>


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="829e4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="829e4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="829e4-109">**хмодуле**</span><span class="sxs-lookup"><span data-stu-id="829e4-109">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="829e4-110">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="829e4-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="829e4-111">Маркер модуля, содержащего загружаемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="829e4-111">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="829e4-112">Если этот член имеет **значение NULL**, ресурс должен быть присоединен к исполняемому файлу, который будет его использовать.</span><span class="sxs-lookup"><span data-stu-id="829e4-112">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="829e4-113">**лпнаме**</span><span class="sxs-lookup"><span data-stu-id="829e4-113">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="829e4-114">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="829e4-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="829e4-115">Указатель на строку, указывающую имя загружаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="829e4-115">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="829e4-116">Например, если ресурс является сеткой, этот член должен указать имя файла сетки.</span><span class="sxs-lookup"><span data-stu-id="829e4-116">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="829e4-117">**лптипе**</span><span class="sxs-lookup"><span data-stu-id="829e4-117">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="829e4-118">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="829e4-118">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="829e4-119">Указатель на строку, указывающую определяемый пользователем тип, идентифицирующий ресурс.</span><span class="sxs-lookup"><span data-stu-id="829e4-119">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="829e4-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="829e4-120">Remarks</span></span>

<span data-ttu-id="829e4-121">Эта структура определяет ресурс для загрузки, когда приложение использует метод [**креатинумобжект**](idirectxfile--createenumobject.md) и указывает дксфилелоад \_ фромресаурце.</span><span class="sxs-lookup"><span data-stu-id="829e4-121">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMRESOURCE.</span></span>

## <a name="requirements"></a><span data-ttu-id="829e4-122">Требования</span><span class="sxs-lookup"><span data-stu-id="829e4-122">Requirements</span></span>



| <span data-ttu-id="829e4-123">Требование</span><span class="sxs-lookup"><span data-stu-id="829e4-123">Requirement</span></span> | <span data-ttu-id="829e4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="829e4-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="829e4-125">Header</span><span class="sxs-lookup"><span data-stu-id="829e4-125">Header</span></span><br/> | <dl> <span data-ttu-id="829e4-126"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="829e4-126"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="829e4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="829e4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829e4-128">Структуры файлов X</span><span class="sxs-lookup"><span data-stu-id="829e4-128">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="829e4-129">**креатинумобжект**</span><span class="sxs-lookup"><span data-stu-id="829e4-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="829e4-130">Константы ДКСФИЛЕ</span><span class="sxs-lookup"><span data-stu-id="829e4-130">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
