---
description: В этом разделе определяются константы, используемые WinHTTP.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Константы WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7c277b4235e23254000766fdef53d25f19ddbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497493"
---
# <a name="winhttp-constants"></a><span data-ttu-id="03983-103">Константы WinHTTP</span><span class="sxs-lookup"><span data-stu-id="03983-103">WinHTTP Constants</span></span>

<span data-ttu-id="03983-104">WinHTTP использует следующие константы:</span><span class="sxs-lookup"><span data-stu-id="03983-104">WinHTTP uses the following constants:</span></span>

<dl> <dt>

[<span data-ttu-id="03983-105">**сообщения об ошибках**</span><span class="sxs-lookup"><span data-stu-id="03983-105">**Error Messages**</span></span>](error-messages.md)
</dt> <dd>

<span data-ttu-id="03983-106">Сообщения об ошибках, относящиеся к функциям WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="03983-106">Error messages specific to the WinHTTP functions.</span></span> <span data-ttu-id="03983-107">Эти функции также возвращают сообщения об ошибках Windows, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="03983-107">These functions also return Windows error messages where appropriate.</span></span> <span data-ttu-id="03983-108">Значение, соответствующее каждой константе, является значением константы для функций интерфейса прикладного программирования (API) и младшими 16 битами номера ошибки для объекта [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="03983-108">The value that corresponds to each constant is the value of the constant for the application programming interface (API) functions and the lower 16 bits of the error number for the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

</dd> <dt>

[<span data-ttu-id="03983-109">**Коды состояния HTTP**</span><span class="sxs-lookup"><span data-stu-id="03983-109">**HTTP Status Codes**</span></span>](http-status-codes.md)
</dt> <dd>

<span data-ttu-id="03983-110">Константы и соответствующие значения, указывающие коды состояния HTTP, возвращаемые серверами в Интернете.</span><span class="sxs-lookup"><span data-stu-id="03983-110">Constants and corresponding values that indicate HTTP status codes returned by servers on the Internet.</span></span>

</dd> <dt>

[<span data-ttu-id="03983-111">**Флаги параметров**</span><span class="sxs-lookup"><span data-stu-id="03983-111">**Option Flags**</span></span>](option-flags.md)
</dt> <dd>

<span data-ttu-id="03983-112">Флаги параметров, поддерживаемые [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) и [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="03983-112">Option flags supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span> <span data-ttu-id="03983-113">Все допустимые флаги параметров имеют значение, большее или равное \_ первому \_ параметру WinHTTP, и меньше или равно \_ последнему \_ параметру WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="03983-113">All valid option flags have a value greater than or equal to WINHTTP\_FIRST\_OPTION and less than or equal to WINHTTP\_LAST\_OPTION.</span></span>

</dd> <dt>

[<span data-ttu-id="03983-114">**\_Порт Интернета**</span><span class="sxs-lookup"><span data-stu-id="03983-114">**INTERNET\_PORT**</span></span>](internet-port.md)
</dt> <dd>

<span data-ttu-id="03983-115">Значение слова, указывающее порт.</span><span class="sxs-lookup"><span data-stu-id="03983-115">A WORD value indicating the port.</span></span>

</dd> <dt>

[<span data-ttu-id="03983-116">**\_схема Интернета**</span><span class="sxs-lookup"><span data-stu-id="03983-116">**INTERNET\_SCHEME**</span></span>](internet-scheme.md)
</dt> <dd>

<span data-ttu-id="03983-117">Схемы Интернета, поддерживаемые WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="03983-117">Internet schemes supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="03983-118">**Флаги сведений о запросе**</span><span class="sxs-lookup"><span data-stu-id="03983-118">**Query Info Flags**</span></span>](query-info-flags.md)
</dt> <dd>

<span data-ttu-id="03983-119">Атрибуты и модификаторы, используемые [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="03983-119">Attributes and modifiers used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

</dd> </dl>

 

 



