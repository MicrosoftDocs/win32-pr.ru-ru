---
description: Определяет матрицу дискретизация.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: Структура DXVA_Qmatrix_HEVC (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 2aba66636717eee5deb04032d9408ace495e1edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539563"
---
# <a name="dxva_qmatrix_hevc-structure"></a><span data-ttu-id="b0444-103">\_ \_ Структура HEVC кматрикс дксва</span><span class="sxs-lookup"><span data-stu-id="b0444-103">DXVA\_Qmatrix\_HEVC structure</span></span>

<span data-ttu-id="b0444-104">Определяет матрицу дискретизация.</span><span class="sxs-lookup"><span data-stu-id="b0444-104">Defines a quantization matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0444-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0444-105">Syntax</span></span>


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a><span data-ttu-id="b0444-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b0444-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b0444-107">**ucScalingLists0 \[ 6 \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="b0444-107">**ucScalingLists0\[6\]\[16\]**</span></span>
</dt> <dd>

<span data-ttu-id="b0444-108">Содержит списки масштабирования для процесса масштабирования 4x4, соответствующие скалинглист \[ 0 \] \[ матриксид \] \[ i \] в спецификации HEVC, где матриксид находится в диапазоне от 0 до 5 включительно, а i находится в диапазоне от 0 до 15 включительно.</span><span class="sxs-lookup"><span data-stu-id="b0444-108">Contains the scaling lists for the 4x4 scaling process, corresponding to ScalingList\[ 0 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 15, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="b0444-109">**ucScalingLists1 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="b0444-109">**ucScalingLists1\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="b0444-110">Содержит списки масштабирования для процесса масштабирования 8x8, соответствующие Скалинглист \[ 1 \] \[ матриксид \] \[ i \] в спецификации HEVC, где матриксид находится в диапазоне от 0 до 5 включительно, а i находится в диапазоне от 0 до 63 включительно.</span><span class="sxs-lookup"><span data-stu-id="b0444-110">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 1 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="b0444-111">**ucScalingLists2 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="b0444-111">**ucScalingLists2\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="b0444-112">Содержит списки масштабирования для процесса масштабирования 8x8, соответствующие Скалинглист \[ 2 \] \[ матриксид \] \[ i \] в спецификации HEVC, где матриксид находится в диапазоне от 0 до 5 включительно, а i находится в диапазоне от 0 до 63 включительно.</span><span class="sxs-lookup"><span data-stu-id="b0444-112">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 2 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="b0444-113">**ucScalingLists3 \[ 2 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="b0444-113">**ucScalingLists3\[2\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="b0444-114">Содержит списки масштабирования для процесса масштабирования 8x8, соответствующие Скалинглист \[ 3 \] \[ матриксид \] \[ i \] в спецификации HEVC, где матриксид находится в диапазоне от 0 до 1 включительно, а i находится в диапазоне от 0 до 63 включительно.</span><span class="sxs-lookup"><span data-stu-id="b0444-114">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 3 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 1, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="b0444-115">**ucScalingListDCCoefSizeID2**</span><span class="sxs-lookup"><span data-stu-id="b0444-115">**ucScalingListDCCoefSizeID2**</span></span>
</dt> <dd>

<span data-ttu-id="b0444-116">Содержит значение контроллера домена в списке масштабирования размером 16x16 с Сизеид, равное 2 и соответствующее в списке масштабирования \_ \_ DC \_ коеф \_ minus8 \[ сизеид − 2 \] \[ матриксид \] + 8 с сизеид, равным 2, и матриксид в диапазоне от 0 до 5 включительно в спецификации HEVC.</span><span class="sxs-lookup"><span data-stu-id="b0444-116">Contains the DC value of the scaling list for 16x16 size with sizeID equal to 2 and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 2 and matrixID in the range of 0 to 5, inclusive, in HEVC specification.</span></span>

</dd> <dt>

<span data-ttu-id="b0444-117">**ucScalingListDCCoefSizeID3**</span><span class="sxs-lookup"><span data-stu-id="b0444-117">**ucScalingListDCCoefSizeID3**</span></span>
</dt> <dd>

<span data-ttu-id="b0444-118">Содержит значение контроллера домена в списке масштабирования размером 32x32 с Сизеид, равное 3, и соответствующее масштабированию \_ List \_ DC \_ коеф \_ minus8 \[ сизеид − 2 \] \[ матриксид \] + 8 с сизеид, равным 3, и матриксид в диапазоне от 0 до 1 включительно в спецификации HEVC.</span><span class="sxs-lookup"><span data-stu-id="b0444-118">Contains the DC value of the scaling list for 32x32 size with sizeID equal to 3, and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 3 and matrixID in the range of 0 to 1, inclusive, in HEVC specification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0444-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b0444-119">Requirements</span></span>



| <span data-ttu-id="b0444-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b0444-120">Requirement</span></span> | <span data-ttu-id="b0444-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b0444-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b0444-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0444-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b0444-123">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0444-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b0444-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0444-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b0444-125">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0444-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b0444-126">Header</span><span class="sxs-lookup"><span data-stu-id="b0444-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0444-127"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0444-127"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0444-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0444-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0444-129">Структуры Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0444-129">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




