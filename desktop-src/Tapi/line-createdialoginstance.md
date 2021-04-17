---
description: Сообщение ТСПИ LINE \_ креатедиалогинстанце заставляет TAPI создать связь между поставщиком службы и экземпляром функции туиспи провидерженерикдиалог, которая \_ выполняется в контексте приложения.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: Сообщение LINE_CREATEDIALOGINSTANCE (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675493"
---
# <a name="line_createdialoginstance-message"></a><span data-ttu-id="74961-103">Строка \_ сообщения креатедиалогинстанце</span><span class="sxs-lookup"><span data-stu-id="74961-103">LINE\_CREATEDIALOGINSTANCE message</span></span>

<span data-ttu-id="74961-104">Сообщение ТСПИ **Line \_ КРЕАТЕДИАЛОГИНСТАНЦЕ** заставляет TAPI создать связь между поставщиком услуг и экземпляром функции [**туиспи \_ провидерженерикдиалог**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) , которая выполняется в контексте приложения, вызвавшего асинхронную функцию Тспи, определяемую параметром *Дврекуестид* структуры [**туиспикреатедиалогинстанцепарамс**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) , на которую указывает *lpTUISPICreateDialogInstanceParams*.</span><span class="sxs-lookup"><span data-stu-id="74961-104">The TSPI **LINE\_CREATEDIALOGINSTANCE** message causes TAPI to create an association between the service provider and an instance of the [**TUISPI\_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) function executing in the context of the application that invoked the asynchronous TSPI function identified by the *dwRequestID* parameter of the [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure pointed to by *lpTUISPICreateDialogInstanceParams*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="74961-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="74961-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74961-106">*хпровидер*</span><span class="sxs-lookup"><span data-stu-id="74961-106">*hProvider*</span></span> 
</dt> <dd>

<span data-ttu-id="74961-107">Провидерхандле, предоставляемый поставщику услуг в качестве параметра для [**тспи \_ провидеренумдевицес**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span><span class="sxs-lookup"><span data-stu-id="74961-107">The ProviderHandle supplied to the service provider as a parameter to [**TSPI\_providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span></span>

</dd> <dt>

<span data-ttu-id="74961-108">*лптуиспикреатедиалогинстанцепарамс*</span><span class="sxs-lookup"><span data-stu-id="74961-108">*lpTUISPICreateDialogInstanceParams*</span></span> 
</dt> <dd>

<span data-ttu-id="74961-109">Указатель на структуру [**туиспикреатедиалогинстанцепарамс**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) .</span><span class="sxs-lookup"><span data-stu-id="74961-109">Pointer to a [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74961-110">Требования</span><span class="sxs-lookup"><span data-stu-id="74961-110">Requirements</span></span>



| <span data-ttu-id="74961-111">Требование</span><span class="sxs-lookup"><span data-stu-id="74961-111">Requirement</span></span> | <span data-ttu-id="74961-112">Значение</span><span class="sxs-lookup"><span data-stu-id="74961-112">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="74961-113">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="74961-113">TAPI version</span></span><br/> | <span data-ttu-id="74961-114">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="74961-114">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="74961-115">Header</span><span class="sxs-lookup"><span data-stu-id="74961-115">Header</span></span><br/>       | <dl> <span data-ttu-id="74961-116"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="74961-116"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74961-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74961-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74961-118">**ТСПИ \_ провидеренумдевицес**</span><span class="sxs-lookup"><span data-stu-id="74961-118">**TSPI\_providerEnumDevices**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[<span data-ttu-id="74961-119">**туиспикреатедиалогинстанцепарамс**</span><span class="sxs-lookup"><span data-stu-id="74961-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

