---
description: Определяет типы устройств.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Перечисление D3DDEVTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694118"
---
# <a name="d3ddevtype-enumeration"></a><span data-ttu-id="4ecca-103">Перечисление D3DDEVTYPE</span><span class="sxs-lookup"><span data-stu-id="4ecca-103">D3DDEVTYPE enumeration</span></span>

<span data-ttu-id="4ecca-104">Определяет типы устройств.</span><span class="sxs-lookup"><span data-stu-id="4ecca-104">Defines device types.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ecca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ecca-105">Syntax</span></span>


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a><span data-ttu-id="4ecca-106">Константы</span><span class="sxs-lookup"><span data-stu-id="4ecca-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4ecca-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE \_ HAL**</span><span class="sxs-lookup"><span data-stu-id="4ecca-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE\_HAL**</span></span>
</dt> <dd>

<span data-ttu-id="4ecca-108">Аппаратное растрирование.</span><span class="sxs-lookup"><span data-stu-id="4ecca-108">Hardware rasterization.</span></span> <span data-ttu-id="4ecca-109">Заливка выполняется программным обеспечением, оборудованием, смешанным преобразованием и освещением.</span><span class="sxs-lookup"><span data-stu-id="4ecca-109">Shading is done with software, hardware, or mixed transform and lighting.</span></span>

</dd> <dt>

<span data-ttu-id="4ecca-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ нуллреф**</span><span class="sxs-lookup"><span data-stu-id="4ecca-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE\_NULLREF**</span></span>
</dt> <dd>

<span data-ttu-id="4ecca-111">Инициализируйте Direct3D на компьютере, на котором нет доступных растровых устройств и ссылок на них, и включите ресурсы для создания трехмерного содержимого.</span><span class="sxs-lookup"><span data-stu-id="4ecca-111">Initialize Direct3D on a computer that has neither hardware nor reference rasterization available, and enable resources for 3D content creation.</span></span> <span data-ttu-id="4ecca-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="4ecca-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4ecca-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ ref**</span><span class="sxs-lookup"><span data-stu-id="4ecca-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE\_REF**</span></span>
</dt> <dd>

<span data-ttu-id="4ecca-114">Функции Direct3D реализуются в программном обеспечении. Однако в этом случае средство программной прорисовки использует специальные инструкции ЦП, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="4ecca-114">Direct3D features are implemented in software; however, the reference rasterizer does make use of special CPU instructions whenever it can.</span></span>

<span data-ttu-id="4ecca-115">Эталонное устройство устанавливается Windows SDK 8,0 или более поздней версии и предназначено для помощи в отладке только для разработки.</span><span class="sxs-lookup"><span data-stu-id="4ecca-115">The reference device is installed by the Windows SDK 8.0 or later and is intended as an aid in debugging for development only.</span></span>

</dd> <dt>

<span data-ttu-id="4ecca-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**</span><span class="sxs-lookup"><span data-stu-id="4ecca-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE\_SW**</span></span>
</dt> <dd>

<span data-ttu-id="4ecca-117">Подключаемое программное устройство, зарегистрированное с помощью [**IDirect3D9:: регистерсофтваредевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span><span class="sxs-lookup"><span data-stu-id="4ecca-117">A pluggable software device that has been registered with [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span></span>

</dd> <dt>

<span data-ttu-id="4ecca-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4ecca-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4ecca-119">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="4ecca-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4ecca-120">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="4ecca-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4ecca-121">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="4ecca-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ecca-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ecca-122">Remarks</span></span>

<span data-ttu-id="4ecca-123">Все методы интерфейса [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) , которые принимают тип устройства **D3DDEVTYPE** , завершатся ошибкой, если \_ задано D3DDEVTYPE нуллреф.</span><span class="sxs-lookup"><span data-stu-id="4ecca-123">All methods of the [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) interface that take a **D3DDEVTYPE** device type will fail if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="4ecca-124">Чтобы использовать эти методы, замените D3DDEVTYPE \_ ref в вызове метода.</span><span class="sxs-lookup"><span data-stu-id="4ecca-124">To use these methods, substitute D3DDEVTYPE\_REF in the method call.</span></span>

<span data-ttu-id="4ecca-125">Устройство D3DDEVTYPE \_ ref должно быть создано в памяти с \_ рабочей областью D3DPOOL, если только не требуются буферы вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="4ecca-125">A D3DDEVTYPE\_REF device should be created in D3DPOOL\_SCRATCH memory, unless vertex and index buffers are required.</span></span> <span data-ttu-id="4ecca-126">Для поддержки буферов вершин и индексов Создайте устройство в памяти D3DPOOL \_ системмем.</span><span class="sxs-lookup"><span data-stu-id="4ecca-126">To support vertex and index buffers, create the device in D3DPOOL\_SYSTEMMEM memory.</span></span>

<span data-ttu-id="4ecca-127">Если установлен D3dref9.dll, Direct3D будет использовать средство программной прорисовки для создания \_ типа устройства D3DDEVTYPE, даже если \_ задано D3DDEVTYPE нуллреф.</span><span class="sxs-lookup"><span data-stu-id="4ecca-127">If D3dref9.dll is installed, Direct3D will use the reference rasterizer to create a D3DDEVTYPE\_REF device type, even if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="4ecca-128">Если D3dref9.dll недоступен и указан параметр D3DDEVTYPE \_ нуллреф, то Direct3D не будет ни визуализировать сцену, ни представлять ее.</span><span class="sxs-lookup"><span data-stu-id="4ecca-128">If D3dref9.dll is not available and D3DDEVTYPE\_NULLREF is specified, Direct3D will neither render nor present the scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ecca-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4ecca-129">Requirements</span></span>



| <span data-ttu-id="4ecca-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4ecca-130">Requirement</span></span> | <span data-ttu-id="4ecca-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4ecca-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecca-132">Header</span><span class="sxs-lookup"><span data-stu-id="4ecca-132">Header</span></span><br/> | <dl> <span data-ttu-id="4ecca-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ecca-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ecca-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ecca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ecca-135">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="4ecca-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="4ecca-136">**IDirect3D9:: Чеккдевицеформат**</span><span class="sxs-lookup"><span data-stu-id="4ecca-136">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[<span data-ttu-id="4ecca-137">**IDirect3D9:: Чеккдевицемултисамплетипе**</span><span class="sxs-lookup"><span data-stu-id="4ecca-137">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[<span data-ttu-id="4ecca-138">**IDirect3D9:: Чеккдевицетипе**</span><span class="sxs-lookup"><span data-stu-id="4ecca-138">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[<span data-ttu-id="4ecca-139">**IDirect3D9:: Креатедевице**</span><span class="sxs-lookup"><span data-stu-id="4ecca-139">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="4ecca-140">**IDirect3D9:: Жетдевицекапс**</span><span class="sxs-lookup"><span data-stu-id="4ecca-140">**IDirect3D9::GetDeviceCaps**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[<span data-ttu-id="4ecca-141">**\_Параметры создания \_ D3DDEVICE**</span><span class="sxs-lookup"><span data-stu-id="4ecca-141">**D3DDEVICE\_CREATION\_PARAMETERS**</span></span>](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
