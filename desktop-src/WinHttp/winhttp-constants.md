---
description: В этом разделе определяются константы, используемые WinHTTP.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Константы WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37b0e4de7aa3df5e155933bea2be25386c1637
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113175006"
---
# <a name="winhttp-constants"></a><span data-ttu-id="36f31-103">Константы WinHTTP</span><span class="sxs-lookup"><span data-stu-id="36f31-103">WinHTTP Constants</span></span>

<span data-ttu-id="36f31-104">WinHTTP использует следующие константы:</span><span class="sxs-lookup"><span data-stu-id="36f31-104">WinHTTP uses the following constants:</span></span>

<dl>

<dt>

[<span data-ttu-id="36f31-105">**сообщения об ошибках**</span><span class="sxs-lookup"><span data-stu-id="36f31-105">**Error Messages**</span></span>](error-messages.md)
</dt> <dd>

<span data-ttu-id="36f31-106">Сообщения об ошибках, относящиеся к функциям WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="36f31-106">Error messages specific to the WinHTTP functions.</span></span> <span data-ttu-id="36f31-107">эти функции также возвращают Windows сообщения об ошибках, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="36f31-107">These functions also return Windows error messages where appropriate.</span></span> <span data-ttu-id="36f31-108">Значение, соответствующее каждой константе, является значением константы для функций интерфейса прикладного программирования (API) и младшими 16 битами номера ошибки для объекта [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="36f31-108">The value that corresponds to each constant is the value of the constant for the application programming interface (API) functions and the lower 16 bits of the error number for the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

</dd> <dt>

[<span data-ttu-id="36f31-109">**Коды состояния HTTP**</span><span class="sxs-lookup"><span data-stu-id="36f31-109">**HTTP Status Codes**</span></span>](http-status-codes.md)
</dt> <dd>

<span data-ttu-id="36f31-110">Константы и соответствующие значения, указывающие коды состояния HTTP, возвращаемые серверами в Интернете.</span><span class="sxs-lookup"><span data-stu-id="36f31-110">Constants and corresponding values that indicate HTTP status codes returned by servers on the Internet.</span></span>

</dd> <dt>

[<span data-ttu-id="36f31-111">**Флаги параметров**</span><span class="sxs-lookup"><span data-stu-id="36f31-111">**Option Flags**</span></span>](option-flags.md)
</dt> <dd>

<span data-ttu-id="36f31-112">Флаги параметров, поддерживаемые [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) и [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="36f31-112">Option flags supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span> <span data-ttu-id="36f31-113">Все допустимые флаги параметров имеют значение, большее или равное \_ первому \_ параметру WinHTTP, и меньше или равно \_ последнему \_ параметру WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="36f31-113">All valid option flags have a value greater than or equal to WINHTTP\_FIRST\_OPTION and less than or equal to WINHTTP\_LAST\_OPTION.</span></span>

</dd> <dt>

[<span data-ttu-id="36f31-114">**\_Порт Интернета**</span><span class="sxs-lookup"><span data-stu-id="36f31-114">**INTERNET\_PORT**</span></span>](internet-port.md)
</dt> <dd>

<span data-ttu-id="36f31-115">Значение слова, указывающее порт.</span><span class="sxs-lookup"><span data-stu-id="36f31-115">A WORD value indicating the port.</span></span>

</dd> <dt>

[<span data-ttu-id="36f31-116">**\_схема Интернета**</span><span class="sxs-lookup"><span data-stu-id="36f31-116">**INTERNET\_SCHEME**</span></span>](internet-scheme.md)
</dt> <dd>

<span data-ttu-id="36f31-117">Схемы Интернета, поддерживаемые WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="36f31-117">Internet schemes supported by WinHTTP.</span></span>

</dd>

<dt>

[<span data-ttu-id="36f31-118">**Флаги сведений о запросе**</span><span class="sxs-lookup"><span data-stu-id="36f31-118">**Query Info Flags**</span></span>](query-info-flags.md)
</dt>
<dd>

<span data-ttu-id="36f31-119">Атрибуты и модификаторы, используемые [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="36f31-119">Attributes and modifiers used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
</dd>

<dt>

<span data-ttu-id="36f31-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span><span class="sxs-lookup"><span data-stu-id="36f31-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span></span>
</dt>
<dd>

<span data-ttu-id="36f31-121">Имеет значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="36f31-121">Has a value of 0x00000001.</span></span> <span data-ttu-id="36f31-122">Указывает, [винхттпаддрекуессеадерсекс](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) , что передаваемые строки являются строками в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="36f31-122">Indicates to [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) that the strings passed in are Unicode strings.</span></span>
</dd>

<dt>

<span data-ttu-id="36f31-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span><span class="sxs-lookup"><span data-stu-id="36f31-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span></span>
</dt>
<dd>

<span data-ttu-id="36f31-124">Имеет значение 0x0000000000000001ull.</span><span class="sxs-lookup"><span data-stu-id="36f31-124">Has a value of 0x0000000000000001ull.</span></span> <span data-ttu-id="36f31-125">Указывает, что [винхттпреаддатаекс](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) не должен завершать вызов до тех пор, пока предоставленный буфер данных не будет заполнен или не завершится ответ.</span><span class="sxs-lookup"><span data-stu-id="36f31-125">Instructs [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) not to complete the call until the provided data buffer has been filled, or the response is complete.</span></span> <span data-ttu-id="36f31-126">Передача этого флага делает поведение **винхттпреаддатаекс** эквивалентным для [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="36f31-126">Passing this flag makes the behavior of **WinHttpReadDataEx** equivalent to that of [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span></span>
</dd>

</dl>
