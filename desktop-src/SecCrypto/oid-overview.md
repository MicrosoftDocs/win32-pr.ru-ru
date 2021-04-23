---
description: Расширяемость достигается за счет использования новых идентификаторов объектов (OID), новых типов кодирования и новых библиотек DLL.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Общие сведения о OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911584"
---
# <a name="oid-overview"></a><span data-ttu-id="1ceeb-103">Общие сведения о OID</span><span class="sxs-lookup"><span data-stu-id="1ceeb-103">OID Overview</span></span>

<span data-ttu-id="1ceeb-104">Расширяемость достигается за счет использования новых [*идентификаторов объектов*](../secgloss/o-gly.md) (OID), новых типов кодирования и новых библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="1ceeb-104">Extensibility is achieved by providing for the use of new [*object identifiers*](../secgloss/o-gly.md) (OIDs), new encoding types, and new DLLs.</span></span>

<span data-ttu-id="1ceeb-105">Идентификаторы объектов CryptoAPI могут принимать любые из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="1ceeb-105">CryptoAPI OIDs can take any of the following forms:</span></span>

-   <span data-ttu-id="1ceeb-106">Числовая строка, например "1.2.3.500.88"</span><span class="sxs-lookup"><span data-stu-id="1ceeb-106">A numeric string such as "1.2.3.500.88"</span></span>
-   <span data-ttu-id="1ceeb-107">Буквенно-цифровая строка, например *MyFunction*</span><span class="sxs-lookup"><span data-stu-id="1ceeb-107">An alphanumeric string such as *MyFunction*</span></span>
-   <span data-ttu-id="1ceeb-108">Константа со значением, меньшим или равным 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="1ceeb-108">A constant with a value that is less than or equal to 0xFFFF.</span></span> <span data-ttu-id="1ceeb-109">Эти константы часто связаны с именем с помощью инструкции **\# define** в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="1ceeb-109">These constants are often associated with a name through the use of a **\#define** statement in a header file.</span></span>

<span data-ttu-id="1ceeb-110">Расширяемые функции принимают OID и аргументы типа кодировки.</span><span class="sxs-lookup"><span data-stu-id="1ceeb-110">Extensible functions accept OID and encoding type arguments.</span></span> <span data-ttu-id="1ceeb-111">Эти функции выполняют поиск в системном реестре библиотеки DLL, связанной с аргументами типа OID и кодировки, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="1ceeb-111">These functions search the system registry to find a DLL associated with the OID and encoding type arguments passed to the function.</span></span> <span data-ttu-id="1ceeb-112">Если библиотека DLL для идентификатора OID найдена, то загружается библиотека DLL и вызывается ее функция.</span><span class="sxs-lookup"><span data-stu-id="1ceeb-112">If a DLL for the OID, encoding type combination is found, the DLL is loaded and its function is called.</span></span> <span data-ttu-id="1ceeb-113">На следующем рисунке показана последовательность для функции [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) :</span><span class="sxs-lookup"><span data-stu-id="1ceeb-113">The following illustration shows this flow for the [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) function:</span></span>

![поток OID](images/oidflow.png)

<span data-ttu-id="1ceeb-115">Это позволяет расширять функциональные возможности CryptoAPI по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="1ceeb-115">This allows the functionality of the CryptoAPI to be extended as the need arises.</span></span> <span data-ttu-id="1ceeb-116">Использование этой методологии полагается на разработчика новых функций, чтобы написать весь необходимый код для этих функций.</span><span class="sxs-lookup"><span data-stu-id="1ceeb-116">Use of this methodology places a burden on the developer of the new functionality to write all the necessary code for that functionality.</span></span> <span data-ttu-id="1ceeb-117">Например, для кодирования некоторой новой структуры данных функция в библиотеке DLL должна выполнять весь процесс кодирования.</span><span class="sxs-lookup"><span data-stu-id="1ceeb-117">To encode some new data structure, for example, the function in the DLL must perform the entire encoding process.</span></span>

 

 
