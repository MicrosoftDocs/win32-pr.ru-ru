---
description: Объект ТУИСПИДЛЛ \_ определен ниже.
ms.assetid: bc0f876d-2443-4c3c-b723-3f82dc6bf849
title: TUISPIDLL_OBJECT_ (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a4711478b98f1ab4983fd8c83a59772e5b370e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675849"
---
# <a name="tuispidll_object_"></a><span data-ttu-id="f00c1-103">\_объект туиспидлл\_</span><span class="sxs-lookup"><span data-stu-id="f00c1-103">TUISPIDLL\_OBJECT\_</span></span>

<dl> <dt>

<span data-ttu-id="f00c1-104"><span id="TUISPIDLL_OBJECT_LINEID"></span><span id="tuispidll_object_lineid"></span>**\_линеид объекта \_ туиспидлл**</span><span class="sxs-lookup"><span data-stu-id="f00c1-104"><span id="TUISPIDLL_OBJECT_LINEID"></span><span id="tuispidll_object_lineid"></span>**TUISPIDLL\_OBJECT\_LINEID**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="f00c1-105">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f00c1-105">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="f00c1-106">*двобжектид* — это идентификатор устройства в виде строки (двдевицеид).</span><span class="sxs-lookup"><span data-stu-id="f00c1-106">*dwObjectID* is a line device identifier (dwDeviceID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f00c1-107"><span id="TUISPIDLL_OBJECT_PHONEID"></span><span id="tuispidll_object_phoneid"></span>**\_фонеид объекта \_ туиспидлл**</span><span class="sxs-lookup"><span data-stu-id="f00c1-107"><span id="TUISPIDLL_OBJECT_PHONEID"></span><span id="tuispidll_object_phoneid"></span>**TUISPIDLL\_OBJECT\_PHONEID**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="f00c1-108">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f00c1-108">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="f00c1-109">*двобжектид* — это идентификатор телефонного устройства (двдевицеид).</span><span class="sxs-lookup"><span data-stu-id="f00c1-109">*dwObjectID* is a phone device identifier (dwDeviceID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f00c1-110"><span id="TUISPIDLL_OBJECT_PROVIDERID"></span><span id="tuispidll_object_providerid"></span>**\_объект PROVIDERID объекта туиспидлл \_**</span><span class="sxs-lookup"><span data-stu-id="f00c1-110"><span id="TUISPIDLL_OBJECT_PROVIDERID"></span><span id="tuispidll_object_providerid"></span>**TUISPIDLL\_OBJECT\_PROVIDERID**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="f00c1-111">0x00000003</span><span class="sxs-lookup"><span data-stu-id="f00c1-111">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="f00c1-112">*двобжектид* — это постоянный идентификатор поставщика.</span><span class="sxs-lookup"><span data-stu-id="f00c1-112">*dwObjectID* is a permanent provider identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f00c1-113"><span id="TUISPIDLL_OBJECT_DIALOGINSTANCE"></span><span id="tuispidll_object_dialoginstance"></span>**\_диалогинстанце объекта \_ туиспидлл**</span><span class="sxs-lookup"><span data-stu-id="f00c1-113"><span id="TUISPIDLL_OBJECT_DIALOGINSTANCE"></span><span id="tuispidll_object_dialoginstance"></span>**TUISPIDLL\_OBJECT\_DIALOGINSTANCE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="f00c1-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f00c1-114">0x00000004</span></span> 
</dt> <dt>



<span data-ttu-id="f00c1-115">*двобжектид* — это обработчик экземпляров диалогового окна (ХДРВДИАЛОГИНСТАНЦЕ или хтапидиалогинстанце, в зависимости от контекста).</span><span class="sxs-lookup"><span data-stu-id="f00c1-115">*dwObjectID* is a dialog instance handle (either HDRVDIALOGINSTANCE or HTAPIDIALOGINSTANCE, depending on the context).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f00c1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f00c1-116">Requirements</span></span>



| <span data-ttu-id="f00c1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f00c1-117">Requirement</span></span> | <span data-ttu-id="f00c1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f00c1-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f00c1-119">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f00c1-119">TAPI version</span></span><br/> | <span data-ttu-id="f00c1-120">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f00c1-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f00c1-121">Header</span><span class="sxs-lookup"><span data-stu-id="f00c1-121">Header</span></span><br/>       | <dl> <span data-ttu-id="f00c1-122"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f00c1-122"><dt>Tspi.h</dt></span></span> </dl> |



 

 




