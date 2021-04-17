---
description: Ксинглефилтертерминал — это дополнительный базовый класс терминала, применимый как к статическим, так и к динамическим терминалам.
ms.assetid: d423438f-1324-4df3-beaa-fdef325fac2e
title: ксинглефилтертерминал
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111a20e59ab0c549e994695610364c451c07fd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683794"
---
# <a name="csinglefilterterminal"></a><span data-ttu-id="547f0-103">ксинглефилтертерминал</span><span class="sxs-lookup"><span data-stu-id="547f0-103">CSingleFilterTerminal</span></span>

<span data-ttu-id="547f0-104">**Ксинглефилтертерминал** — это дополнительный базовый класс терминала, применимый как к статическим, так и к динамическим терминалам.</span><span class="sxs-lookup"><span data-stu-id="547f0-104">**CSingleFilterTerminal** is an additional terminal base class applicable to both static and dynamic terminals.</span></span> <span data-ttu-id="547f0-105">Он является производным от [**кбасетерминал**](cbaseterminal.md) и делает реализацию более конкретной, предполагая, что у терминала есть один фильтр DirectShow.</span><span class="sxs-lookup"><span data-stu-id="547f0-105">It is derived from [**CBaseTerminal**](cbaseterminal.md) and makes the implementation more specific by assuming that the terminal has a single DirectShow filter.</span></span> <span data-ttu-id="547f0-106">При выполнении этого условия создание производной реализации терминала от **ксинглефилтертерминал** намного проще, чем наследование от **кбасетерминал**.</span><span class="sxs-lookup"><span data-stu-id="547f0-106">When this condition is met, deriving a terminal implementation from **CSingleFilterTerminal** is much easier than deriving from **CBaseTerminal**.</span></span>

<span data-ttu-id="547f0-107">Определен в Мсптерм. h.</span><span class="sxs-lookup"><span data-stu-id="547f0-107">Defined in MSPterm.h.</span></span>

 

 



