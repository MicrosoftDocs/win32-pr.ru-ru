---
description: Описывает параметры создания для устройства.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: Структура D3DDEVICE_CREATION_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 72b2f35f1666ec2095c6ea8f5d5588dc7fd62f2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354473"
---
# <a name="d3ddevice_creation_parameters-structure"></a><span data-ttu-id="9713f-103">\_ \_ Структура параметров создания D3DDEVICE</span><span class="sxs-lookup"><span data-stu-id="9713f-103">D3DDEVICE\_CREATION\_PARAMETERS structure</span></span>

<span data-ttu-id="9713f-104">Описывает параметры создания для устройства.</span><span class="sxs-lookup"><span data-stu-id="9713f-104">Describes the creation parameters for a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9713f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9713f-105">Syntax</span></span>


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="9713f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9713f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9713f-107">**адаптерординал**</span><span class="sxs-lookup"><span data-stu-id="9713f-107">**AdapterOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="9713f-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9713f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9713f-109">Порядковый номер, обозначающий адаптер дисплея.</span><span class="sxs-lookup"><span data-stu-id="9713f-109">Ordinal number that denotes the display adapter.</span></span> <span data-ttu-id="9713f-110">D3DADAPTER \_ по умолчанию всегда является основным видеоадаптером.</span><span class="sxs-lookup"><span data-stu-id="9713f-110">D3DADAPTER\_DEFAULT is always the primary display adapter.</span></span> <span data-ttu-id="9713f-111">Используйте это порядковое числитель в качестве параметра адаптера для любого из методов [**IDirect3D9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="9713f-111">Use this ordinal as the Adapter parameter for any of the [**IDirect3D9**](/windows/desktop/api) methods.</span></span> <span data-ttu-id="9713f-112">Обратите внимание, что разные экземпляры объектов Direct3D 9,0 могут использовать разные порядковые номера.</span><span class="sxs-lookup"><span data-stu-id="9713f-112">Note that different instances of Direct3D 9.0 objects can use different ordinals.</span></span> <span data-ttu-id="9713f-113">Адаптеры могут вводить или оставлять систему в том случае, если пользователи, например, добавляют или удаляют мониторы из системы с несколькими мониторами или при горячей замене ноутбука.</span><span class="sxs-lookup"><span data-stu-id="9713f-113">Adapters can enter or leave a system when users, for example, add or remove monitors from a multiple-monitor system or when they hot-swap a laptop.</span></span> <span data-ttu-id="9713f-114">Следовательно, используйте это порядковое имя только в экземпляре Direct3D 9,0, известном как допустимый, то есть в Direct3D 9,0, который создал этот интерфейс [**IDirect3DDevice9**](/windows/desktop/api) , или Direct3D 9,0, возвращенном из [**Direct3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), как вызвано через этот интерфейс **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="9713f-114">Consequently, use this ordinal only in a Direct3D 9.0 instance known to be valid, that is, either the Direct3D 9.0 that created this [**IDirect3DDevice9**](/windows/desktop/api) interface or the Direct3D 9.0 returned from [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), as called through this **IDirect3DDevice9** interface.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-115">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="9713f-115">**DeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="9713f-116">Тип: **[ **D3DDEVTYPE**](./d3ddevtype.md)**</span><span class="sxs-lookup"><span data-stu-id="9713f-116">Type: **[**D3DDEVTYPE**](./d3ddevtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9713f-117">Член перечисляемого типа [**D3DDEVTYPE**](./d3ddevtype.md) .</span><span class="sxs-lookup"><span data-stu-id="9713f-117">Member of the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type.</span></span> <span data-ttu-id="9713f-118">Обозначает количество эмулированных функций для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="9713f-118">Denotes the amount of emulated functionality for this device.</span></span> <span data-ttu-id="9713f-119">Значение этого параметра отражает значение, передаваемое в вызов [**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) , который создал это устройство.</span><span class="sxs-lookup"><span data-stu-id="9713f-119">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-120">**хфокусвиндов**</span><span class="sxs-lookup"><span data-stu-id="9713f-120">**hFocusWindow**</span></span>
</dt> <dd>

<span data-ttu-id="9713f-121">Тип: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9713f-121">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9713f-122">Маркер окна, к которому относится фокус для этого устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9713f-122">Window handle to which focus belongs for this Direct3D device.</span></span> <span data-ttu-id="9713f-123">Значение этого параметра отражает значение, передаваемое в вызов [**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) , который создал это устройство.</span><span class="sxs-lookup"><span data-stu-id="9713f-123">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-124">**бехавиорфлагс**</span><span class="sxs-lookup"><span data-stu-id="9713f-124">**BehaviorFlags**</span></span>
</dt> <dd>

<span data-ttu-id="9713f-125">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9713f-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9713f-126">Сочетание одной или нескольких констант [D3DCREATE](d3dcreate.md) , управляющих глобальным поведением устройства.</span><span class="sxs-lookup"><span data-stu-id="9713f-126">A combination of one or more [D3DCREATE](d3dcreate.md) constants that control global behavior of the device.</span></span> <span data-ttu-id="9713f-127">Эти константы отражают константы, передаваемые в [**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) при создании устройства.</span><span class="sxs-lookup"><span data-stu-id="9713f-127">These constants mirror the constants passed to [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) when the device was created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9713f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9713f-128">Requirements</span></span>



| <span data-ttu-id="9713f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9713f-129">Requirement</span></span> | <span data-ttu-id="9713f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9713f-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9713f-131">Header</span><span class="sxs-lookup"><span data-stu-id="9713f-131">Header</span></span><br/> | <dl> <span data-ttu-id="9713f-132"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9713f-132"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9713f-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9713f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9713f-134">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="9713f-134">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="9713f-135">**жеткреатионпараметерс**</span><span class="sxs-lookup"><span data-stu-id="9713f-135">**GetCreationParameters**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[<span data-ttu-id="9713f-136">**креатедевице**</span><span class="sxs-lookup"><span data-stu-id="9713f-136">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
