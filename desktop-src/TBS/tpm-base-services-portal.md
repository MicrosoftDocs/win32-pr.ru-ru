---
title: Базовые службы TPM
description: Программное обеспечение TPM предоставляет службы как API, предоставляемые через удаленный вызов процедур. Используйте TPM, чтобы создать модуль TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- TBS базовых служб TPM
- TBS базовых служб TPM, Домашняя страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413327"
---
# <a name="tpm-base-services"></a><span data-ttu-id="d3c9e-106">Базовые службы TPM</span><span class="sxs-lookup"><span data-stu-id="d3c9e-106">TPM Base Services</span></span>

## <a name="purpose"></a><span data-ttu-id="d3c9e-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="d3c9e-107">Purpose</span></span>

<span data-ttu-id="d3c9e-108">Функция базовых служб доверенный платформенный модуль (TPM) (TPM) централизует доступ к TPM между приложениями.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-108">The Trusted Platform Module (TPM) Base Services (TBS) feature centralizes TPM access across applications.</span></span>

<span data-ttu-id="d3c9e-109">Функция TBS работает как системная служба в Windows Server 2008, Windows Vista или более поздних операционных системах.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-109">The TBS feature runs as a system service in Windows Server 2008, Windows Vista, or newer operating systems.</span></span> <span data-ttu-id="d3c9e-110">Он предоставляет службы как API, предоставляемые через удаленные вызовы процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="d3c9e-110">It provides services as an API exposed through remote procedure calls (RPC).</span></span> <span data-ttu-id="d3c9e-111">Функция TBS использует приоритеты, указанные в вызове приложений для совместного планирования доступа к TPM.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-111">The TBS feature uses priorities specified by calling applications to cooperatively schedule TPM access.</span></span>

> [!Note]
>
> <span data-ttu-id="d3c9e-112">TPM можно использовать для операций с хранилищем ключей.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-112">The TPM can be used for key storage operations.</span></span> <span data-ttu-id="d3c9e-113">Тем не менее разработчикам рекомендуется использовать [API хранилища ключей](/windows/desktop/SecCNG/key-storage-and-retrieval) для этих сценариев.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-113">However, developers are encouraged to use the [Key Storage APIs](/windows/desktop/SecCNG/key-storage-and-retrieval) for these scenarios instead.</span></span> <span data-ttu-id="d3c9e-114">API хранилища ключей предоставляют функциональные возможности для создания, подписывания или шифрования с помощью и сохранения криптографических ключей, а также более высокого уровня и более удобны для использования, чем TBS для этих целевых сценариев.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-114">The Key Storage APIs provide the functionality to create, sign or encrypt with, and persist cryptographic keys, and they are higher-level and easier to use than the TBS for these targeted scenarios.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="d3c9e-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="d3c9e-115">Developer audience</span></span>

<span data-ttu-id="d3c9e-116">TBS предназначен для разработчиков приложений, использующих операционные системы Windows.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-116">TBS is intended for use by developers of applications based on the Windows operating systems.</span></span> <span data-ttu-id="d3c9e-117">Разработчики должны быть знакомы с языками программирования C и C++ и средой программирования Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-117">Developers should be familiar with the C and C++ programming languages and the Microsoft Windows programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d3c9e-118">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="d3c9e-118">Run-time requirements</span></span>

<span data-ttu-id="d3c9e-119">Для функции TBS требуется как минимум операционная система Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-119">The TBS feature requires at least Windows Server 2008 or Windows Vista operating system.</span></span> <span data-ttu-id="d3c9e-120">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-120">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d3c9e-121">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d3c9e-121">In this section</span></span>



| <span data-ttu-id="d3c9e-122">Раздел</span><span class="sxs-lookup"><span data-stu-id="d3c9e-122">Topic</span></span>                                         | <span data-ttu-id="d3c9e-123">Описание</span><span class="sxs-lookup"><span data-stu-id="d3c9e-123">Description</span></span>                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="d3c9e-124">О TBS</span><span class="sxs-lookup"><span data-stu-id="d3c9e-124">About TBS</span></span>](about-tbs.md)<br/>         | <span data-ttu-id="d3c9e-125">Основные понятия и обобщенное представление функции TBS.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-125">Key concepts and a high-level view of the TBS feature.</span></span><br/>               |
| [<span data-ttu-id="d3c9e-126">Использование TBS</span><span class="sxs-lookup"><span data-stu-id="d3c9e-126">Using TBS</span></span>](using-tbs.md)<br/>         | <span data-ttu-id="d3c9e-127">Процессы и процедуры TBS для использования API TBS.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-127">TBS processes and procedures for using the TBS API.</span></span><br/>                  |
| [<span data-ttu-id="d3c9e-128">Справочник по TBS</span><span class="sxs-lookup"><span data-stu-id="d3c9e-128">TBS Reference</span></span>](tbs-reference.md)<br/> | <span data-ttu-id="d3c9e-129">Документация по функциям TBS, структурам и кодам возврата.</span><span class="sxs-lookup"><span data-stu-id="d3c9e-129">Documentation about the TBS functions, structures, and return codes.</span></span><br/> |



 

 

