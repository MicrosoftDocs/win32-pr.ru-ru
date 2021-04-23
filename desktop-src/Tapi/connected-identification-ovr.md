---
description: Подключенная идентификация определяет субъект, к которому фактически подключился. Это может отличаться от вызываемой идентификации, если вызов был передан.
ms.assetid: 3f9ba728-8e78-4f1f-a0c1-76799fd62c9d
title: Подключенная идентификация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fdb2f11b27bf9281b381170aa0d5b5ab027088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350565"
---
# <a name="connected-identification"></a><span data-ttu-id="bb790-104">Подключенная идентификация</span><span class="sxs-lookup"><span data-stu-id="bb790-104">Connected Identification</span></span>

<span data-ttu-id="bb790-105">Подключенная идентификация определяет субъект, к которому фактически подключился.</span><span class="sxs-lookup"><span data-stu-id="bb790-105">The connected identification identifies the party that was actually connected to.</span></span> <span data-ttu-id="bb790-106">Это может отличаться от вызываемой идентификации, если вызов был передан.</span><span class="sxs-lookup"><span data-stu-id="bb790-106">This may be different from the called identification if the call was diverted.</span></span>

<span data-ttu-id="bb790-107">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="bb790-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="bb790-108">**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**двконнектедидфлагс**, **двконнектедидсизе**, **двконнектедидоффсет**, **двконнектедиднамесизе** и **dwConnectedIDNameOffset** lpCallInfo *).*</span><span class="sxs-lookup"><span data-stu-id="bb790-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**, **dwConnectedIDSize**, **dwConnectedIDOffset**, **dwConnectedIDNameSize**, and **dwConnectedIDNameOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="bb790-109">**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфостринг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (элемент **CIL \_ коннектедиднаме** [**каллинфо \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="bb790-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL\_CONNECTEDIDNAME** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
