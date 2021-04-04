---
description: Следующие функции реализуются библиотекой DLL поставщика сети для взаимодействия с маршрутизатором нескольких поставщиков (MPR).
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Функции, реализованные поставщиками сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999308"
---
# <a name="functions-implemented-by-network-providers"></a><span data-ttu-id="85fdf-103">Функции, реализованные поставщиками сети</span><span class="sxs-lookup"><span data-stu-id="85fdf-103">Functions Implemented by Network Providers</span></span>

<span data-ttu-id="85fdf-104">Следующие функции реализуются библиотекой DLL поставщика сети для взаимодействия с [*маршрутизатором нескольких поставщиков*](/windows/desktop/SecGloss/m-gly) (MPR).</span><span class="sxs-lookup"><span data-stu-id="85fdf-104">The following functions are implemented by a network provider DLL to communicate with the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR).</span></span> <span data-ttu-id="85fdf-105">Обратите внимание, что поставщик сети должен реализовать только [функции возможностей](capabilities-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="85fdf-105">Note that only the [Capabilities Functions](capabilities-functions.md) must be implemented by a network provider.</span></span> <span data-ttu-id="85fdf-106">Реализация других типов функций является необязательной и зависит от требований поставщика сети.</span><span class="sxs-lookup"><span data-stu-id="85fdf-106">Implementation of the other types of functions is optional and depends on the requirements of the network provider.</span></span>



| <span data-ttu-id="85fdf-107">Набор функций</span><span class="sxs-lookup"><span data-stu-id="85fdf-107">Function set</span></span>                                                                                    | <span data-ttu-id="85fdf-108">Описание</span><span class="sxs-lookup"><span data-stu-id="85fdf-108">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85fdf-109">Функции возможностей</span><span class="sxs-lookup"><span data-stu-id="85fdf-109">Capabilities Functions</span></span>](capabilities-functions.md)<br/>                                 | <span data-ttu-id="85fdf-110">Позволяет вызывающему объекту определить возможности поставщика сети.</span><span class="sxs-lookup"><span data-stu-id="85fdf-110">Allows the caller to determine the capabilities of the network provider.</span></span><br/>                                                                |
| [<span data-ttu-id="85fdf-111">Функции имени пользователя</span><span class="sxs-lookup"><span data-stu-id="85fdf-111">User Name Functions</span></span>](user-name-functions.md)<br/>                                       | <span data-ttu-id="85fdf-112">Запрашивает у поставщика сети имя пользователя, связанное с подключением.</span><span class="sxs-lookup"><span data-stu-id="85fdf-112">Prompts the network provider for the user name associated with a connection.</span></span><br/>                                                            |
| [<span data-ttu-id="85fdf-113">Функции перенаправления устройств</span><span class="sxs-lookup"><span data-stu-id="85fdf-113">Device-Redirecting Functions</span></span>](device-redirecting-functions.md)<br/>                     | <span data-ttu-id="85fdf-114">Позволяет поставщику сети перенаправлять устройства, буквы дисков и порты LPT, которые являются стандартными в операционной системе Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="85fdf-114">Allows a network provider to redirect devices, drive letters, and LPT ports that are standard on the Microsoft MS-DOS operating system.</span></span><br/> |
| [<span data-ttu-id="85fdf-115">Зависящие от поставщика функции диалогового окна</span><span class="sxs-lookup"><span data-stu-id="85fdf-115">Provider-Specific Dialog Box Functions</span></span>](provider-specific-dialog-box-functions.md)<br/> | <span data-ttu-id="85fdf-116">Позволяет поставщику сети отображать сведения, относящиеся к сети, или работать с ними.</span><span class="sxs-lookup"><span data-stu-id="85fdf-116">Allows a network provider to display or act on network-specific information.</span></span><br/>                                                            |
| [<span data-ttu-id="85fdf-117">Административные функции</span><span class="sxs-lookup"><span data-stu-id="85fdf-117">Administrative Functions</span></span>](administrative-functions.md)<br/>                             | <span data-ttu-id="85fdf-118">Позволяет поставщику сети отображать специальные сетевые каталоги или работать с ними.</span><span class="sxs-lookup"><span data-stu-id="85fdf-118">Allows a network provider to display or act on special network directories.</span></span><br/>                                                             |
| [<span data-ttu-id="85fdf-119">Функции перечисления</span><span class="sxs-lookup"><span data-stu-id="85fdf-119">Enumeration Functions</span></span>](enumeration-functions.md)<br/>                                   | <span data-ttu-id="85fdf-120">Позволяет пользователю просматривать сетевые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="85fdf-120">Allows the user to browse network resources.</span></span><br/>                                                                                            |



 

<span data-ttu-id="85fdf-121">Дополнительные сведения о создании и регистрации поставщика сети см. в статьях [Реализация поставщика](implementing-a-network-provider.md) сети и [Регистрация поставщиков сетевых услуг и диспетчеров учетных данных](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="85fdf-121">For more information about how to create and register a network provider, see [Implementing a Network Provider](implementing-a-network-provider.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

