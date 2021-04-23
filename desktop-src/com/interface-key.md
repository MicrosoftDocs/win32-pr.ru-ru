---
title: Ключ интерфейса
description: Регистрирует новые интерфейсы, сопоставляя имя интерфейса с ИДЕНТИФИКАТОРом интерфейса (IID). Для каждого нового интерфейса должен существовать один подраздел IID.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Раздел реестра интерфейса COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068333"
---
# <a name="interface-key"></a><span data-ttu-id="64ff4-105">Ключ интерфейса</span><span class="sxs-lookup"><span data-stu-id="64ff4-105">Interface Key</span></span>

<span data-ttu-id="64ff4-106">Регистрирует новые интерфейсы, сопоставляя имя интерфейса с ИДЕНТИФИКАТОРом интерфейса (IID).</span><span class="sxs-lookup"><span data-stu-id="64ff4-106">Registers new interfaces by associating an interface name with an interface ID (IID).</span></span> <span data-ttu-id="64ff4-107">Для каждого нового интерфейса должен существовать один подраздел IID.</span><span class="sxs-lookup"><span data-stu-id="64ff4-107">There must be one IID subkey for each new interface.</span></span>

## <a name="registry-key"></a><span data-ttu-id="64ff4-108">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="64ff4-108">Registry Key</span></span>

<span data-ttu-id="64ff4-109">**HKey \_ \_ \\ Классы программного \\ обеспечения \\ локального компьютера — интерфейс** \\ *{* IID *}*</span><span class="sxs-lookup"><span data-stu-id="64ff4-109">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Interface**\\ *{* IID *}*</span></span>



| <span data-ttu-id="64ff4-110">Значение реестра</span><span class="sxs-lookup"><span data-stu-id="64ff4-110">Registry value</span></span>                               | <span data-ttu-id="64ff4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="64ff4-111">Description</span></span>                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64ff4-112">**BaseInterface**</span><span class="sxs-lookup"><span data-stu-id="64ff4-112">**BaseInterface**</span></span>](baseinterface.md)       | <span data-ttu-id="64ff4-113">Определяет интерфейс, производным от которого является текущий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="64ff4-113">Identifies the interface from which the current interface is derived.</span></span>                                  |
| [<span data-ttu-id="64ff4-114">**нуммесодс**</span><span class="sxs-lookup"><span data-stu-id="64ff4-114">**NumMethods**</span></span>](nummethods.md)             | <span data-ttu-id="64ff4-115">Содержит число методов в связанном интерфейсе, включая методы из производных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="64ff4-115">Contains the number of methods in the associated interface, including methods from derived interfaces.</span></span> |
| [<span data-ttu-id="64ff4-116">**проксистубклсид**</span><span class="sxs-lookup"><span data-stu-id="64ff4-116">**ProxyStubClsid**</span></span>](proxystubclsid.md)     | <span data-ttu-id="64ff4-117">Сопоставляет идентификатор IID с идентификатором CLSID в 16-разрядных прокси-библиотеках.</span><span class="sxs-lookup"><span data-stu-id="64ff4-117">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>                                                           |
| [<span data-ttu-id="64ff4-118">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="64ff4-118">**ProxyStubClsid32**</span></span>](proxystubclsid32.md) | <span data-ttu-id="64ff4-119">Сопоставляет идентификатор IID с идентификатором CLSID в 32-разрядных прокси-библиотеках.</span><span class="sxs-lookup"><span data-stu-id="64ff4-119">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="64ff4-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64ff4-120">Remarks</span></span>

<span data-ttu-id="64ff4-121">Ключ **\_ \_ \\ \\ классов программного обеспечения файла hKey на локальном компьютере** соответствует **\_ \_ корневому ключу classes** , который был сохранен для совместимости с предыдущими версиями com.</span><span class="sxs-lookup"><span data-stu-id="64ff4-121">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64ff4-122">См. также</span><span class="sxs-lookup"><span data-stu-id="64ff4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64ff4-123">**Взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="64ff4-123">**Interface**</span></span>](interface.md)
</dt> </dl>

 

 




