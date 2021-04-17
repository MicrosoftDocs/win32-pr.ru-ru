---
description: Параметры для перечисления режимов вывода.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664962"
---
# <a name="dxgi_enum_modes"></a><span data-ttu-id="565bd-103">\_режимы ПЕРЕЧИСЛЕНИЯ \_ DXGI</span><span class="sxs-lookup"><span data-stu-id="565bd-103">DXGI\_ENUM\_MODES</span></span>

<span data-ttu-id="565bd-104">Параметры для перечисления режимов вывода.</span><span class="sxs-lookup"><span data-stu-id="565bd-104">Options for enumerating display modes.</span></span>



| <span data-ttu-id="565bd-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="565bd-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="565bd-106">Описание</span><span class="sxs-lookup"><span data-stu-id="565bd-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <span data-ttu-id="565bd-107"><dt>**DXGI \_ Режимы ПЕРЕЧИСЛЕНИЯ с \_ \_ чередованием**</dt> <dt>1UL</dt></span><span class="sxs-lookup"><span data-stu-id="565bd-107"><dt>**DXGI\_ENUM\_MODES\_INTERLACED**</dt> <dt>1UL</dt></span></span> </dl>                 | <span data-ttu-id="565bd-108">Включить чередующиеся режимы.</span><span class="sxs-lookup"><span data-stu-id="565bd-108">Include interlaced modes.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <span data-ttu-id="565bd-109"><dt>**DXGI \_ \_ \_ Масштабирование режимов перечисления**</dt> <dt>2UL</dt></span><span class="sxs-lookup"><span data-stu-id="565bd-109"><dt>**DXGI\_ENUM\_MODES\_SCALING**</dt> <dt>2UL</dt></span></span> </dl>                          | <span data-ttu-id="565bd-110">Включите режимы растяжения и масштабирования.</span><span class="sxs-lookup"><span data-stu-id="565bd-110">Include stretched-scaling modes.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <span data-ttu-id="565bd-111"><dt>**DXGI \_ \_Режимы перечисления \_ стерео**</dt> <dt>4UL</dt></span><span class="sxs-lookup"><span data-stu-id="565bd-111"><dt>**DXGI\_ENUM\_MODES\_STEREO**</dt> <dt>4UL</dt></span></span> </dl>                             | <span data-ttu-id="565bd-112">Включение стерео режимов.</span><span class="sxs-lookup"><span data-stu-id="565bd-112">Include stereo modes.</span></span><br/> <span data-ttu-id="565bd-113">**Direct3D 11:** Это значение перечисления поддерживается начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="565bd-113">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <span data-ttu-id="565bd-114"><dt>**DXGI \_ \_Режимы перечисления \_ отключили \_ стерео**</dt> <dt>8UL</dt></span><span class="sxs-lookup"><span data-stu-id="565bd-114"><dt>**DXGI\_ENUM\_MODES\_DISABLED\_STEREO**</dt> <dt>8UL</dt></span></span> </dl> | <span data-ttu-id="565bd-115">Включить стерео-режимы, которые скрыты, так как пользователь отключил стерео.</span><span class="sxs-lookup"><span data-stu-id="565bd-115">Include stereo modes that are hidden because the user has disabled stereo.</span></span> <span data-ttu-id="565bd-116">Приложения панели управления могут использовать этот параметр для отображения возможностей стерео, отключенных в рамках пользовательского интерфейса, который включает и отключает стерео.</span><span class="sxs-lookup"><span data-stu-id="565bd-116">Control panel applications can use this option to show stereo capabilities that have been disabled as part of a user interface that enables and disables stereo.</span></span><br/> <span data-ttu-id="565bd-117">**Direct3D 11:** Это значение перечисления поддерживается начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="565bd-117">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="565bd-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="565bd-118">Remarks</span></span>

<span data-ttu-id="565bd-119">Эти параметры флага используются в [**идксгиаутпут:: жетдисплаймоделист**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) для перечисления режимов вывода.</span><span class="sxs-lookup"><span data-stu-id="565bd-119">These flag options are used in [**IDXGIOutput::GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) to enumerate display modes.</span></span>

<span data-ttu-id="565bd-120">Эти параметры флагов также используются в [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) для перечисления режимов вывода.</span><span class="sxs-lookup"><span data-stu-id="565bd-120">These flag options are also used in [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) to enumerate display modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="565bd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="565bd-121">Requirements</span></span>



| <span data-ttu-id="565bd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="565bd-122">Requirement</span></span> | <span data-ttu-id="565bd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="565bd-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="565bd-124">Header</span><span class="sxs-lookup"><span data-stu-id="565bd-124">Header</span></span><br/> | <dl> <span data-ttu-id="565bd-125"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="565bd-125"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="565bd-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="565bd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="565bd-127">Константы DXGI</span><span class="sxs-lookup"><span data-stu-id="565bd-127">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




