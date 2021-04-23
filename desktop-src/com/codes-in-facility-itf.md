---
title: Коды в FACILITY_ITF
description: Коды в СРЕДСТВе \_ ИТФ
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986311"
---
# <a name="codes-in-facility_itf"></a><span data-ttu-id="d75b0-103">Коды в СРЕДСТВе \_ ИТФ</span><span class="sxs-lookup"><span data-stu-id="d75b0-103">Codes in FACILITY\_ITF</span></span>

<span data-ttu-id="d75b0-104">**HRESULT** s с такими средствами, как \_ null и механизм \_ RPC, имеют универсальное значение, так как они определены в одном источнике: Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d75b0-104">**HRESULT** s with facilities such as FACILITY\_NULL and FACILITY\_RPC have universal meaning because they are defined at a single source: Microsoft.</span></span> <span data-ttu-id="d75b0-105">Однако **HRESULTS** в \_ итфе устройства определяются методом функции или интерфейса, из которой они возвращаются.</span><span class="sxs-lookup"><span data-stu-id="d75b0-105">However, **HRESULT** s in FACILITY\_ITF are determined by the function or interface method from which they are returned.</span></span> <span data-ttu-id="d75b0-106">Это означает, что одно и то же 32-разрядное значение в СРЕДСТВе \_ ИТФ, возвращаемое из двух разных методов интерфейса, может иметь разные значения.</span><span class="sxs-lookup"><span data-stu-id="d75b0-106">This means that the same 32-bit value in FACILITY\_ITF returned from two different interface methods might have different meanings.</span></span>

<span data-ttu-id="d75b0-107">Причина, по которой **значения HRESULT** в \_ итфе устройства могут иметь разные значения в разных интерфейсах, заключается в том, что **HRESULT** s сохраняется в эффективный размер типа данных 32 бит.</span><span class="sxs-lookup"><span data-stu-id="d75b0-107">The reason **HRESULT** s in FACILITY\_ITF can have different meanings in different interfaces is that **HRESULT** s are kept to an efficient data type size of 32 bits.</span></span> <span data-ttu-id="d75b0-108">К сожалению, 32 бит недостаточно велик для разработки системы выделения кода ошибки, которая позволяет избежать конфликтующих кодов, выделенных разными программистами в разные моменты в разных местах (в отличие от обработки идентификаторов интерфейсов и CLSID).</span><span class="sxs-lookup"><span data-stu-id="d75b0-108">Unfortunately, 32 bits is not large enough for the development of an error code allocation system that avoids conflicting codes allocated by different programmers at different times in different places (unlike the handling of interface identifiers and CLSIDs).</span></span> <span data-ttu-id="d75b0-109">В результате 32-разрядное **значение HRESULT** структурировано таким образом, что корпорация Майкрософт может определить несколько универсальных кодов ошибок, в то же время позволяя другим программистам определять новые коды ошибок, не опасаясь конфликтов.</span><span class="sxs-lookup"><span data-stu-id="d75b0-109">As a result, the 32-bit **HRESULT** is structured such that Microsoft can define several universal error codes, while allowing other programmers to define new error codes without fear of conflict.</span></span> <span data-ttu-id="d75b0-110">Соглашение о коде состояния выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d75b0-110">The status code convention is as follows:</span></span>

-   <span data-ttu-id="d75b0-111">Коды состояния в средствах, отличных от \_ ИТФ оборудования, могут определяться только корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d75b0-111">Status codes in facilities other than FACILITY\_ITF can be defined only by Microsoft.</span></span>
-   <span data-ttu-id="d75b0-112">Коды состояния в СРЕДСТВАх \_ ИТФ определяются исключительно разработчиком интерфейса или функции, возвращающей код состояния.</span><span class="sxs-lookup"><span data-stu-id="d75b0-112">Status codes in facility FACILITY\_ITF are defined solely by the developer of the interface or function that returns the status code.</span></span> <span data-ttu-id="d75b0-113">Чтобы избежать возникновения конфликтующих кодов ошибок, кто-то определяет, что интерфейс отвечает за координацию и публикацию \_ кодов состояния итфов устройств, связанных с этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="d75b0-113">To avoid conflicting error codes, whoever defines the interface is responsible for coordinating and publishing the FACILITY\_ITF status codes associated with that interface.</span></span>

<span data-ttu-id="d75b0-114">Все коды ИТФ средств, определяемые моделью COM, \_ имеют значение кода в диапазоне Символ 0x0000-0x01FF.</span><span class="sxs-lookup"><span data-stu-id="d75b0-114">All the COM-defined FACILITY\_ITF codes have a code value in the range of 0x0000-0x01FF.</span></span> <span data-ttu-id="d75b0-115">Хотя можно использовать любые коды в СРЕДСТВе \_ ИТФ, рекомендуется использовать только значения кода в диапазоне 0x0200-0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="d75b0-115">While it is legal to use any codes in FACILITY\_ITF, it is recommended that only code values in the range of 0x0200-0xFFFF be used.</span></span> <span data-ttu-id="d75b0-116">Эта рекомендация является средством сокращения путаницы с ошибками, определенными в COM.</span><span class="sxs-lookup"><span data-stu-id="d75b0-116">This recommendation is made as a means of reducing confusion with any COM-defined errors.</span></span>

<span data-ttu-id="d75b0-117">Также рекомендуется, чтобы разработчики определяли новые функции и интерфейсы для возврата кодов ошибок в соответствии с определением COM и средствами, отличными от \_ ИТФ.</span><span class="sxs-lookup"><span data-stu-id="d75b0-117">It is also recommended that developers define new functions and interfaces to return error codes as defined by COM and in facilities other than FACILITY\_ITF.</span></span> <span data-ttu-id="d75b0-118">В частности, интерфейсы с любой вероятностью удаленного использования RPC в будущем должны определять \_ Допустимые коды RPC.</span><span class="sxs-lookup"><span data-stu-id="d75b0-118">In particular, interfaces that have any chance of being remoted using RPC in the future should define the FACILITY\_RPC codes as legal.</span></span> <span data-ttu-id="d75b0-119">\_Неожиданный код ошибки, который большинство разработчиков будет использовать для универсального юридического лица.</span><span class="sxs-lookup"><span data-stu-id="d75b0-119">E\_UNEXPECTED is a specific error code that most developers will want to make universally legal.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d75b0-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d75b0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d75b0-121">Обработка ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="d75b0-121">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




