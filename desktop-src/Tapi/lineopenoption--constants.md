---
description: В \_ константах линеопеноптион перечислены доступные параметры для открытия строки.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Константы LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679663"
---
# <a name="lineopenoption_-constants"></a><span data-ttu-id="0f108-103">\_Константы линеопеноптион</span><span class="sxs-lookup"><span data-stu-id="0f108-103">LINEOPENOPTION\_ Constants</span></span>

<span data-ttu-id="0f108-104">В **\_ константах линеопеноптион** перечислены доступные параметры для открытия строки.</span><span class="sxs-lookup"><span data-stu-id="0f108-104">The **LINEOPENOPTION\_ constants** list the available options for opening a line.</span></span>

<dl> <dt>

<span data-ttu-id="0f108-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_прокси-сервер линеопеноптион**</span><span class="sxs-lookup"><span data-stu-id="0f108-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0f108-106">Приложение предназначено для обработки запросов от других приложений, в которых линия открыта.</span><span class="sxs-lookup"><span data-stu-id="0f108-106">The application is willing to handle requests from other applications that have the line open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0f108-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**ЛИНЕОПЕНОПТИОН \_ синглеаддресс**</span><span class="sxs-lookup"><span data-stu-id="0f108-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION\_SINGLEADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0f108-108">Приложение должно информировать о новых вызовах, созданных на устройстве, только в том случае, если эти вызовы появляются по адресу, указанному в элементе **дваддрессид** в структуре [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) , на которую указывает параметр *лпкаллпарамс* .</span><span class="sxs-lookup"><span data-stu-id="0f108-108">The application should be informed of new calls created on the line device only if those calls appear on the address specified in the **dwAddressID** member in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure pointed to by the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f108-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f108-109">Remarks</span></span>

<span data-ttu-id="0f108-110">Дополнительные сведения о работе этих параметров см. в разделе [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen) .</span><span class="sxs-lookup"><span data-stu-id="0f108-110">See [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f108-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0f108-111">Requirements</span></span>



| <span data-ttu-id="0f108-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0f108-112">Requirement</span></span> | <span data-ttu-id="0f108-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0f108-113">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0f108-114">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="0f108-114">TAPI version</span></span><br/> | <span data-ttu-id="0f108-115">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0f108-115">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0f108-116">Header</span><span class="sxs-lookup"><span data-stu-id="0f108-116">Header</span></span><br/>       | <dl> <span data-ttu-id="0f108-117"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f108-117"><dt>Tapi.h</dt></span></span> </dl> |



 

 




