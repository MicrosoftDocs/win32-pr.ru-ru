---
description: Сообщение ТСПИ LINE \_ сенддиалогинстанцедата заставляет TAPI вызывать \_ функцию туиспи ПРОВИДЕРЖЕНЕРИКДИАЛОГДАТА в DLL пользовательского интерфейса, связанной с хтдлгинст, передав блок параметров, на который указывает лппарамс, длиной двсизе.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: Сообщение LINE_SENDDIALOGINSTANCEDATA (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689398"
---
# <a name="line_senddialoginstancedata-message"></a><span data-ttu-id="7715c-103">Строка \_ сообщения сенддиалогинстанцедата</span><span class="sxs-lookup"><span data-stu-id="7715c-103">LINE\_SENDDIALOGINSTANCEDATA message</span></span>

<span data-ttu-id="7715c-104">Сообщение ТСПИ **Line \_ СЕНДДИАЛОГИНСТАНЦЕДАТА** заставляет TAPI вызывать функцию [**туиспи \_ провидерженерикдиалогдата**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) в DLL пользовательского интерфейса, связанной с *хтдлгинст*, передав блок параметров, на который указывает *лппарамс*, длиной *двсизе*.</span><span class="sxs-lookup"><span data-stu-id="7715c-104">The TSPI **LINE\_SENDDIALOGINSTANCEDATA** message causes TAPI to call the [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function in the UI DLL associated with *htDlgInst*, passing it the parameter block pointed to by *lpParams*, of length *dwSize*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7715c-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="7715c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7715c-106">*хтдлгинст*</span><span class="sxs-lookup"><span data-stu-id="7715c-106">*htDlgInst*</span></span> 
</dt> <dd>

<span data-ttu-id="7715c-107">ХТАПИДИАЛОГИНСТАНЦЕ, возвращенный поставщику услуг, когда экземпляр диалогового окна был создан с помощью [**Line \_ креатедиалогинстанце**](line-createdialoginstance.md).</span><span class="sxs-lookup"><span data-stu-id="7715c-107">The HTAPIDIALOGINSTANCE that was returned to the service provider when the dialog box instance was created using [**LINE\_CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="7715c-108">*лппарамс*</span><span class="sxs-lookup"><span data-stu-id="7715c-108">*lpParams*</span></span> 
</dt> <dd>

<span data-ttu-id="7715c-109">Указатель на блок параметров, зависящий от поставщика, который передается в функцию [**туиспи \_ провидерженерикдиалогдата**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) пользовательского интерфейса DLL, размер которой указан в *двсизе*.</span><span class="sxs-lookup"><span data-stu-id="7715c-109">Pointer to a provider-specific parameter block that is conveyed to the UI DLL [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function, the size of which is specified by *dwSize*.</span></span> <span data-ttu-id="7715c-110">Если этот параметр имеет значение **null**, это запрос на немедленное закрытие диалогового окна и очистку (библиотека DLL пользовательского интерфейса не должна вызывать [**туиспидллкаллбакк**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) во время этой очистки).</span><span class="sxs-lookup"><span data-stu-id="7715c-110">If this parameter is set to **NULL**, this is a request to close the dialog box immediately and clean up (the UI DLL should not invoke [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) during this cleanup).</span></span>

</dd> <dt>

<span data-ttu-id="7715c-111">*двсизе*</span><span class="sxs-lookup"><span data-stu-id="7715c-111">*dwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7715c-112">Размер в байтах блока параметров, который должен быть передан в библиотеку DLL пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7715c-112">The size in bytes of the parameter block to be conveyed to the UI DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7715c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7715c-113">Requirements</span></span>



| <span data-ttu-id="7715c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7715c-114">Requirement</span></span> | <span data-ttu-id="7715c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7715c-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7715c-116">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="7715c-116">TAPI version</span></span><br/> | <span data-ttu-id="7715c-117">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7715c-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7715c-118">Header</span><span class="sxs-lookup"><span data-stu-id="7715c-118">Header</span></span><br/>       | <dl> <span data-ttu-id="7715c-119"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7715c-119"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7715c-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7715c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7715c-121">**туиспидллкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7715c-121">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[<span data-ttu-id="7715c-122">**ТУИСПИ \_ провидерженерикдиалогдата**</span><span class="sxs-lookup"><span data-stu-id="7715c-122">**TUISPI\_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[<span data-ttu-id="7715c-123">**Строка \_ креатедиалогинстанце**</span><span class="sxs-lookup"><span data-stu-id="7715c-123">**LINE\_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
</dt> </dl>

 

