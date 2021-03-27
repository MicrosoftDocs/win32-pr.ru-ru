---
description: В этом разделе описываются макросы служебной программы оболочки Windows.
title: Макросы оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5be120f4-bf5d-44b3-b508-20a2104655fa
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 085bca918cfa6ca1441272c3c9181226ef603ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998762"
---
# <a name="shell-macros"></a><span data-ttu-id="a8ac8-103">Макросы оболочки</span><span class="sxs-lookup"><span data-stu-id="a8ac8-103">Shell Macros</span></span>

<span data-ttu-id="a8ac8-104">В этом разделе описываются макросы служебной программы оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-104">This section describes the Windows Shell utility macros.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a8ac8-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="a8ac8-105">In this section</span></span>



| <span data-ttu-id="a8ac8-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="a8ac8-106">Topic</span></span>                                                                  | <span data-ttu-id="a8ac8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a8ac8-107">Description</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8ac8-108">**ОПРЕДЕЛЕНИЕ \_ PROPERTYKEY**</span><span class="sxs-lookup"><span data-stu-id="a8ac8-108">**DEFINE\_PROPERTYKEY**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-define_propertykey)<br/>           | <span data-ttu-id="a8ac8-109">Используется для упаковки идентификатора формата (FMTID) и идентификатора свойства (PID) в структуру [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) , представляющую ключ свойства.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-109">Used to pack a format identifier (FMTID) and property identifier (PID) into a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure that represents a property key.</span></span><br/>                                                                                    |
| [<span data-ttu-id="a8ac8-110">**IID \_ ППВ \_ args**</span><span class="sxs-lookup"><span data-stu-id="a8ac8-110">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)<br/>                      | <span data-ttu-id="a8ac8-111">Используется для получения указателя на интерфейс, который автоматически предоставляет значение IID запрошенного интерфейса на основе типа используемого указателя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-111">Used to retrieve an interface pointer, supplying the IID value of the requested interface automatically based on the type of the interface pointer used.</span></span> <span data-ttu-id="a8ac8-112">Это позволяет избежать распространенной ошибки кодирования, проверяя тип значения, передаваемого во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-112">This avoids a common coding error by checking the type of the value passed at compile time.</span></span><br/> |
| [<span data-ttu-id="a8ac8-113">**исекуалпропертикэй**</span><span class="sxs-lookup"><span data-stu-id="a8ac8-113">**IsEqualPropertyKey**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-isequalpropertykey)<br/>            | <span data-ttu-id="a8ac8-114">Сравнивает элементы двух структур [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) и возвращает, равны ли они.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-114">Compares the members of two [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structures and returns whether they are equal.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="a8ac8-115">**македллверулл**</span><span class="sxs-lookup"><span data-stu-id="a8ac8-115">**MAKEDLLVERULL**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)<br/>                      | <span data-ttu-id="a8ac8-116">Используется для упаковки сведений о версии библиотеки DLL в значение УЛОНГЛОНГ.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-116">Used to pack DLL version information into a ULONGLONG value.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="a8ac8-117">**Нетаддр \_ дисплайеррортип**</span><span class="sxs-lookup"><span data-stu-id="a8ac8-117">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)<br/> | <span data-ttu-id="a8ac8-118">Отображает сообщение об ошибке в всплывающей подсказке, связанной с элементом управления "сетевой адрес".</span><span class="sxs-lookup"><span data-stu-id="a8ac8-118">Displays an error message in the balloon tip associated with the network address control.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="a8ac8-119">**Нетаддр \_**</span><span class="sxs-lookup"><span data-stu-id="a8ac8-119">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)<br/>           | <span data-ttu-id="a8ac8-120">Указывает, соответствует ли сетевой адрес указанному типу и формату.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-120">Indicates whether a network address conforms to a specified type and format.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="a8ac8-121">**Нетаддр \_ жеталловтипе**</span><span class="sxs-lookup"><span data-stu-id="a8ac8-121">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)<br/>       | <span data-ttu-id="a8ac8-122">Извлекает типы сетевых адресов, принимаемые указанным элементом управления сетью.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-122">Retrieves the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="a8ac8-123">**Нетаддр \_ сеталловтипе**</span><span class="sxs-lookup"><span data-stu-id="a8ac8-123">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)<br/>       | <span data-ttu-id="a8ac8-124">Задает типы сетевых адресов, принимаемые указанным элементом управления для сетевых адресов.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-124">Sets the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                     |



 

 

 
