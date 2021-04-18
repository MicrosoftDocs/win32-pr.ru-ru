---
title: Различные константы службы текстового ввода TSF (Ктффунк. h)
description: В текстовых службах используются следующие значения.
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ebd7d22f9cfbd59f95ee3dcfe68229536503b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682049"
---
# <a name="miscellaneous-tsf-text-service-constants"></a><span data-ttu-id="c796b-103">Различные константы службы текстового ввода TSF</span><span class="sxs-lookup"><span data-stu-id="c796b-103">Miscellaneous TSF Text Service Constants</span></span>

<span data-ttu-id="c796b-104">В текстовых службах используются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c796b-104">The following values are used with text services.</span></span>



| <span data-ttu-id="c796b-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="c796b-105">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="c796b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c796b-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <span data-ttu-id="c796b-107"><dt>**Tf \_ МЕНУРЕАДИ**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c796b-107"><dt>**TF\_MENUREADY**</dt> <dt>0x00000001</dt></span></span> </dl>                                                | <span data-ttu-id="c796b-108">В настоящий момент не используется.</span><span class="sxs-lookup"><span data-stu-id="c796b-108">Not currently used.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <span data-ttu-id="c796b-109"><dt>**Tf \_ \_Состояние пропуи \_ SAVETOFILE**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c796b-109"><dt>**TF\_PROPUI\_STATUS\_SAVETOFILE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="c796b-110">Свойство может быть сериализовано.</span><span class="sxs-lookup"><span data-stu-id="c796b-110">The property can be serialized.</span></span> <span data-ttu-id="c796b-111">Если это значение отсутствует, свойство не может быть сериализовано.</span><span class="sxs-lookup"><span data-stu-id="c796b-111">If this value is not present, the property cannot be serialized.</span></span> <span data-ttu-id="c796b-112">Это значение используется с [итффнпропертюистатус::-Status](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) и [Итффнпропертюистатус:: SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).</span><span class="sxs-lookup"><span data-stu-id="c796b-112">This value is used with [ITfFnPropertyUIStatus::GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) and [ITfFnPropertyUIStatus::SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c796b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c796b-113">Requirements</span></span>



| <span data-ttu-id="c796b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c796b-114">Requirement</span></span> | <span data-ttu-id="c796b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c796b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c796b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c796b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c796b-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c796b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c796b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c796b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c796b-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c796b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c796b-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c796b-120">Redistributable</span></span><br/>          | <span data-ttu-id="c796b-121">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="c796b-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="c796b-122">Header</span><span class="sxs-lookup"><span data-stu-id="c796b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c796b-123"><dt>Ктффунк. h</dt></span><span class="sxs-lookup"><span data-stu-id="c796b-123"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="c796b-124">IDL</span><span class="sxs-lookup"><span data-stu-id="c796b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c796b-125"><dt>Ктффунк. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c796b-125"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c796b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c796b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c796b-127">Итффнпропертюистатус::/Status</span><span class="sxs-lookup"><span data-stu-id="c796b-127">ITfFnPropertyUIStatus::GetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[<span data-ttu-id="c796b-128">Итффнпропертюистатус:: SetStatus</span><span class="sxs-lookup"><span data-stu-id="c796b-128">ITfFnPropertyUIStatus::SetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





