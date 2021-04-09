---
description: Указывает тип процесса, определенного в \_ \_ выходной структуре D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесс.
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: Перечисление D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143183"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a><span data-ttu-id="f538f-103">\_Перечисление ПРОЦЕССИДЕНТИФИЕРТИПЕ D3DAUTHENTICATEDCHANNEL</span><span class="sxs-lookup"><span data-stu-id="f538f-103">D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE enumeration</span></span>

<span data-ttu-id="f538f-104">Указывает тип процесса, определенного в [**\_ \_ выходной структуре D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесс**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) .</span><span class="sxs-lookup"><span data-stu-id="f538f-104">Specifies the type of process that is identified in the [**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f538f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f538f-105">Syntax</span></span>


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a><span data-ttu-id="f538f-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f538f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f538f-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**ПРОЦЕССИДТИПЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="f538f-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="f538f-108">Неизвестный тип процесса.</span><span class="sxs-lookup"><span data-stu-id="f538f-108">Unknown process type.</span></span>

</dd> <dt>

<span data-ttu-id="f538f-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**ПРОЦЕССИДТИПЕ \_ DWM**</span><span class="sxs-lookup"><span data-stu-id="f538f-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE\_DWM**</span></span>
</dt> <dd>

<span data-ttu-id="f538f-110">Процесс диспетчер окон рабочего стола (DWM).</span><span class="sxs-lookup"><span data-stu-id="f538f-110">Desktop Window Manager (DWM) process.</span></span>

</dd> <dt>

<span data-ttu-id="f538f-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**ПРОЦЕССИДТИПЕ, \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="f538f-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="f538f-112">Обработка процесса.</span><span class="sxs-lookup"><span data-stu-id="f538f-112">Handle to a process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f538f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f538f-113">Requirements</span></span>



| <span data-ttu-id="f538f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f538f-114">Requirement</span></span> | <span data-ttu-id="f538f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f538f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f538f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f538f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f538f-117">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f538f-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f538f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f538f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f538f-119">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f538f-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f538f-120">Header</span><span class="sxs-lookup"><span data-stu-id="f538f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f538f-121"><dt>D3d9types. h (включение D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f538f-121"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f538f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f538f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f538f-123">Перечисления видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="f538f-123">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




