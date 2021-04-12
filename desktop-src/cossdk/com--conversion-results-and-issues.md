---
description: Если вы решили преобразовать пакеты MTS в приложения COM+ вручную или позволить процессу программы установки Microsoft Windows автоматически выполнять эту задачу, следует учитывать результаты преобразования, а также проблемы.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Результаты и проблемы преобразования COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423502"
---
# <a name="com-conversion-results-and-issues"></a><span data-ttu-id="1a822-103">Результаты и проблемы преобразования COM+</span><span class="sxs-lookup"><span data-stu-id="1a822-103">COM+ Conversion Results and Issues</span></span>

<span data-ttu-id="1a822-104">Если вы решили преобразовать пакеты MTS в приложения COM+ вручную или позволить процессу программы установки Microsoft Windows автоматически выполнять эту задачу, следует учитывать результаты преобразования, а также проблемы.</span><span class="sxs-lookup"><span data-stu-id="1a822-104">Whether you choose to convert your MTS packages to COM+ applications manually or let the Microsoft Windows setup process do it for you automatically, you should be aware of the results of conversion as well as the issues.</span></span>

## <a name="what-is-converted"></a><span data-ttu-id="1a822-105">Что преобразуется</span><span class="sxs-lookup"><span data-stu-id="1a822-105">What Is Converted</span></span>

<span data-ttu-id="1a822-106">Во время преобразования служебная программа МТСТОКОМ преобразует роли, назначения ролей, интерфейсы, методы, пользователей, список компьютеров и большинство параметров компьютера.</span><span class="sxs-lookup"><span data-stu-id="1a822-106">During conversion, the MTSTOCOM utility converts roles, role assignments, interfaces, methods, users, the computer list, and most computer settings.</span></span> <span data-ttu-id="1a822-107">Служебная программа МТСТОКОМ также преобразует удостоверение и пароль для пакета MTS.</span><span class="sxs-lookup"><span data-stu-id="1a822-107">The MTSTOCOM utility also converts the identity and password for an MTS package.</span></span>

<span data-ttu-id="1a822-108">Новые атрибуты COM+, недоступные в MTS, автоматически устанавливаются в следующие значения по умолчанию для всех преобразованных компонентов MTS.</span><span class="sxs-lookup"><span data-stu-id="1a822-108">The new COM+ attributes that were not available in MTS are automatically set to the following defaults for all converted MTS components.</span></span> <span data-ttu-id="1a822-109">Эти значения по умолчанию можно изменить с помощью средства администрирования "службы компонентов" или административных интерфейсов COM+.</span><span class="sxs-lookup"><span data-stu-id="1a822-109">These defaults can be changed using either the Component Services administrative tool or the COM+ administrative interfaces.</span></span>

-   <span data-ttu-id="1a822-110">Активирована JIT-активация.</span><span class="sxs-lookup"><span data-stu-id="1a822-110">JIT activation enabled.</span></span>
-   <span data-ttu-id="1a822-111">Пул объектов отключен.</span><span class="sxs-lookup"><span data-stu-id="1a822-111">Object pooling disabled.</span></span>
-   <span data-ttu-id="1a822-112">Синхронизация аналогична параметру транзакции.</span><span class="sxs-lookup"><span data-stu-id="1a822-112">Synchronization same as Transaction setting.</span></span>

## <a name="conversion-issues"></a><span data-ttu-id="1a822-113">Проблемы преобразования</span><span class="sxs-lookup"><span data-stu-id="1a822-113">Conversion Issues</span></span>

<span data-ttu-id="1a822-114">COM+ устанавливается автоматически при установке Windows.</span><span class="sxs-lookup"><span data-stu-id="1a822-114">COM+ is automatically installed when you install Windows.</span></span> <span data-ttu-id="1a822-115">Удалить COM+ невозможно.</span><span class="sxs-lookup"><span data-stu-id="1a822-115">It is not possible to uninstall COM+.</span></span> <span data-ttu-id="1a822-116">Ниже перечислены проблемы, связанные с обновлением существующих установок MTS и COM+.</span><span class="sxs-lookup"><span data-stu-id="1a822-116">Issues related to upgrades of existing MTS and COM+ installations include the following:</span></span>

-   <span data-ttu-id="1a822-117">Если в настоящее время используется MTS 1,0, то MTS автоматически обновляется до COM+.</span><span class="sxs-lookup"><span data-stu-id="1a822-117">If you are currently using MTS 1.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="1a822-118">Однако пользовательские пакеты будут потеряны, и их необходимо будет создать повторно.</span><span class="sxs-lookup"><span data-stu-id="1a822-118">However, user-defined packages will be lost and you must re-create them.</span></span>
-   <span data-ttu-id="1a822-119">Если в настоящее время используется MTS 2,0, то MTS автоматически обновляется до COM+.</span><span class="sxs-lookup"><span data-stu-id="1a822-119">If you are currently using MTS 2.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="1a822-120">Все определяемые пользователем пакеты будут обновлены до приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="1a822-120">All user-defined packages will be upgraded to COM+ applications.</span></span> <span data-ttu-id="1a822-121">Все компоненты должны работать, как и в MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="1a822-121">All components should work as they did under MTS 2.0.</span></span>
-   <span data-ttu-id="1a822-122">Если вы используете MTS 1,0 и MTS 2,0 и установили параметр пакета SDK, файлы пакета SDK будут удалены.</span><span class="sxs-lookup"><span data-stu-id="1a822-122">If you are using MTS 1.0 and MTS 2.0 and have installed the SDK option, the SDK files will be removed.</span></span> <span data-ttu-id="1a822-123">Последнюю версию пакета SDK для COM+ можно установить с помощью Microsoft Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1a822-123">You can install the latest COM+ SDK through the Microsoft Windows SDK.</span></span>
-   <span data-ttu-id="1a822-124">Управлять удаленным компьютером MTS с компьютера COM+ нельзя.</span><span class="sxs-lookup"><span data-stu-id="1a822-124">You cannot manage a remote MTS computer from a COM+ computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a822-125">См. также</span><span class="sxs-lookup"><span data-stu-id="1a822-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a822-126">Автоматическое преобразование из MTS</span><span class="sxs-lookup"><span data-stu-id="1a822-126">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="1a822-127">Ручное преобразование из MTS</span><span class="sxs-lookup"><span data-stu-id="1a822-127">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="1a822-128">Библиотека администрирования MTS</span><span class="sxs-lookup"><span data-stu-id="1a822-128">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



