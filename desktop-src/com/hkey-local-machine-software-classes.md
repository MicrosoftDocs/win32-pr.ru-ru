---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: Подразделы и значения реестра, связанные с \_ ключом " \_ классы программного обеспечения локального компьютера" hKey, \\ \\ содержат сведения о приложении, которое требуется для поддержки COM-функций.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c16fdbc97b32d01af9c96b5670cb5a19c09c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779634"
---
# <a name="hkey_local_machinesoftwareclasses"></a><span data-ttu-id="70d73-103">\_ \_ \\ Классы программного обеспечения для локального компьютера hKey \\</span><span class="sxs-lookup"><span data-stu-id="70d73-103">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes</span></span>

<span data-ttu-id="70d73-104">Подразделы и значения реестра, связанные с ключом " **\_ \_ \\ \\ классы программного обеспечения локального компьютера" hKey** , содержат сведения о приложении, которое требуется для поддержки COM-функций.</span><span class="sxs-lookup"><span data-stu-id="70d73-104">The subkeys and registry values associated with the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key contain information about an application that is needed to support COM functionality.</span></span> <span data-ttu-id="70d73-105">Эти сведения включают в себя такие разделы, как Поддерживаемые форматы данных, сведения о совместимости, программные идентификаторы, DCOM и элементы управления.</span><span class="sxs-lookup"><span data-stu-id="70d73-105">This information includes such topics as supported data formats, compatibility information, programmatic identifiers, DCOM, and controls.</span></span>



| <span data-ttu-id="70d73-106">Подраздел</span><span class="sxs-lookup"><span data-stu-id="70d73-106">Subkey</span></span>                                                                         | <span data-ttu-id="70d73-107">Описание</span><span class="sxs-lookup"><span data-stu-id="70d73-107">Description</span></span>                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70d73-108">**ИД**</span><span class="sxs-lookup"><span data-stu-id="70d73-108">**AppID**</span></span>](appid-key.md)                                                     | <span data-ttu-id="70d73-109">Параметры конфигурации для приложений на основе COM.</span><span class="sxs-lookup"><span data-stu-id="70d73-109">Configuration options for COM-based applications.</span></span>                                                                 |
| [<span data-ttu-id="70d73-110">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="70d73-110">**CLSID**</span></span>](clsid-key-hklm.md)                                                | <span data-ttu-id="70d73-111">Параметры конфигурации для COM-классов.</span><span class="sxs-lookup"><span data-stu-id="70d73-111">Configuration options for COM classes.</span></span>                                                                            |
| [<span data-ttu-id="70d73-112">**<\_ расширение файла>**</span><span class="sxs-lookup"><span data-stu-id="70d73-112">**<file\_extension>**</span></span>](-file-extension--key.md)                        | <span data-ttu-id="70d73-113">Связывает расширение имени файла с ProgID.</span><span class="sxs-lookup"><span data-stu-id="70d73-113">Associates a file name extension with a ProgID.</span></span>                                                                   |
| [<span data-ttu-id="70d73-114">**FileType**</span><span class="sxs-lookup"><span data-stu-id="70d73-114">**FileType**</span></span>](filetype-key.md)                                               | <span data-ttu-id="70d73-115">Используется [**жетклассфиле**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) для сопоставления шаблонов с различными байтами файлов в несоставном файле.</span><span class="sxs-lookup"><span data-stu-id="70d73-115">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span> |
| [<span data-ttu-id="70d73-116">**Интерфейс**</span><span class="sxs-lookup"><span data-stu-id="70d73-116">**Interface**</span></span>](interface-key.md)                                             | <span data-ttu-id="70d73-117">Связывает имя интерфейса с ИДЕНТИФИКАТОРом интерфейса (IID).</span><span class="sxs-lookup"><span data-stu-id="70d73-117">Associates an interface name with an interface ID (IID).</span></span>                                                          |
| [**<ProgID>**](-progid--key.md)                                         | <span data-ttu-id="70d73-118">Определяет класс.</span><span class="sxs-lookup"><span data-stu-id="70d73-118">Identifies a class.</span></span> <span data-ttu-id="70d73-119">Обратите внимание, что идентификатор ProgID не обязательно должен быть глобально уникальным, в отличие от идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="70d73-119">Note that the ProgID is not guaranteed to be globally unique, unlike a CLSID.</span></span>                 |
| [<span data-ttu-id="70d73-120">**<независимый от версии идентификатор ProgID>**</span><span class="sxs-lookup"><span data-stu-id="70d73-120">**<version-independent ProgID>**</span></span>](-version-independent-progid--key.md) | <span data-ttu-id="70d73-121">Используется для определения последней версии объектного приложения.</span><span class="sxs-lookup"><span data-stu-id="70d73-121">Used to determine the latest version of an object application.</span></span>                                                    |



 

 

 




