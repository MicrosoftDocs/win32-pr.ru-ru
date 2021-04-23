---
description: TAPI предоставляет ряд функций для управления дескрипторами вызовов, определения связей между строками, вызовами, адресами и т. д.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Обработка обработки вызовов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683152"
---
# <a name="call-handle-manipulation"></a><span data-ttu-id="e66c0-103">Обработка обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="e66c0-103">Call Handle Manipulation</span></span>

<span data-ttu-id="e66c0-104">TAPI предоставляет ряд функций для управления дескрипторами вызовов, определения связей между строками, вызовами, адресами и т. д.</span><span class="sxs-lookup"><span data-stu-id="e66c0-104">TAPI provides a number of functions for manipulating call handles, determining the relationship among lines, calls, and address, and so on.</span></span> <span data-ttu-id="e66c0-105">Большая часть этой функциональности реализована строго в TAPI без обращения к поставщику услуг, за исключением [**тспи \_ линежеткалладдрессид**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span><span class="sxs-lookup"><span data-stu-id="e66c0-105">Most of this functionality is implemented strictly within TAPI without reference to the service provider, except for [**TSPI\_lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span></span> <span data-ttu-id="e66c0-106">Эта функция получает идентификатор адреса существующего вызова в строке.</span><span class="sxs-lookup"><span data-stu-id="e66c0-106">This function retrieves the address identifier of an existing call within its line.</span></span> <span data-ttu-id="e66c0-107">Поставщики услуг, которые моделируют линию как группу идентификаторов адресов, могут выбрать непредсказуемый адрес для нового входящего или исходящего вызова.</span><span class="sxs-lookup"><span data-stu-id="e66c0-107">Service providers that model a line as a group of address identifiers can choose an unpredictable address for a new inbound or outbound call.</span></span> <span data-ttu-id="e66c0-108">Эта функция предоставляет интерфейсу TAPI достаточную информацию для реализации операции [**линежетневкаллс**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) при вызове с \_ параметром линекаллселект Address.</span><span class="sxs-lookup"><span data-stu-id="e66c0-108">This function gives TAPI sufficient information to implement the [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) operation when it is invoked with the LINECALLSELECT\_ADDRESS option.</span></span>

 

 
