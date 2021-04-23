---
description: Описывает ключ обратного вызова для использования в анимации по ключевым кадрам.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: Структура D3DXKEY_CALLBACK (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5c2c4dc90cbb95218268bf673204867f5b5d6636
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703782"
---
# <a name="d3dxkey_callback-structure"></a><span data-ttu-id="0a025-103">\_Структура обратного вызова D3DXKEY</span><span class="sxs-lookup"><span data-stu-id="0a025-103">D3DXKEY\_CALLBACK structure</span></span>

<span data-ttu-id="0a025-104">Описывает ключ обратного вызова для использования в анимации по ключевым кадрам.</span><span class="sxs-lookup"><span data-stu-id="0a025-104">Describes a callback key for use in key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a025-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a025-105">Syntax</span></span>


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a><span data-ttu-id="0a025-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0a025-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0a025-107">**Time**</span><span class="sxs-lookup"><span data-stu-id="0a025-107">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="0a025-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a025-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0a025-109">Метка времени ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="0a025-109">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="0a025-110">**пкаллбаккдата**</span><span class="sxs-lookup"><span data-stu-id="0a025-110">**pCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="0a025-111">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a025-111">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0a025-112">Указатель на данные обратного вызова пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a025-112">Pointer to user callback data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a025-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0a025-113">Requirements</span></span>



| <span data-ttu-id="0a025-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0a025-114">Requirement</span></span> | <span data-ttu-id="0a025-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0a025-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a025-116">Header</span><span class="sxs-lookup"><span data-stu-id="0a025-116">Header</span></span><br/> | <dl> <span data-ttu-id="0a025-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a025-117"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a025-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a025-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a025-119">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="0a025-119">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
