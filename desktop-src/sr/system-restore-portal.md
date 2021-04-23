---
title: "\"Восстановление системы\""
description: Задает точки восстановления системы и следит за основными изменениями системы от программы, чтобы обеспечить откат системы к предыдущему состоянию. Создайте код автоматического восстановления или скрипт WMI для восстановления состояния системы в зарегистрированную точку восстановления.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- "\"Восстановление системы\""
- Восстановление системы, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134167"
---
# <a name="system-restore"></a><span data-ttu-id="02693-106">"Восстановление системы"</span><span class="sxs-lookup"><span data-stu-id="02693-106">System Restore</span></span>

## <a name="purpose"></a><span data-ttu-id="02693-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="02693-107">Purpose</span></span>

<span data-ttu-id="02693-108">Восстановление системы автоматически отслеживает и регистрирует ключевые изменения системы на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="02693-108">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="02693-109">Он предназначен для уменьшения затрат на поддержку и повышения удовлетворенности клиентов, позволяя пользователю отменить изменения, которые могли вызвать проблему с системой, или вернуться к дню, когда система была оптимальной.</span><span class="sxs-lookup"><span data-stu-id="02693-109">It is designed to reduce support costs and increase customer satisfaction by enabling a user to undo a change that may have caused a problem with the system, or revert to a day when the system was performing optimally.</span></span>

> [!Note]  
> <span data-ttu-id="02693-110">Следующая документация предназначена для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="02693-110">The following documentation is targeted for developers.</span></span> <span data-ttu-id="02693-111">Если вы хотите узнать, как использовать восстановление системы, обратитесь к разделу [что такое восстановление системы?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span><span class="sxs-lookup"><span data-stu-id="02693-111">If you are an end-user looking for information on how to use System Restore, see [What Is System Restore?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="02693-112">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="02693-112">Developer audience</span></span>

<span data-ttu-id="02693-113">API восстановления системы предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="02693-113">The System Restore API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="02693-114">Для использования интерфейса сценариев требуется знание инструментарий управления Windows (WMI) (инструментарий WMI).</span><span class="sxs-lookup"><span data-stu-id="02693-114">A familiarity with Windows Management Instrumentation (WMI) is required to use the scripting interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="02693-115">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="02693-115">Run-time requirements</span></span>

<span data-ttu-id="02693-116">API восстановления системы поддерживается в клиентских операционных системах, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="02693-116">The System Restore API is supported on client operating systems starting with Windows XP.</span></span> <span data-ttu-id="02693-117">Сведения о том, какие операционные системы требуются для использования определенного элемента API, см. в разделе требования документации.</span><span class="sxs-lookup"><span data-stu-id="02693-117">For information about which operating systems are required to use a particular API element, see the Requirements section of its documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="02693-118">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="02693-118">In this section</span></span>



| <span data-ttu-id="02693-119">Раздел</span><span class="sxs-lookup"><span data-stu-id="02693-119">Topic</span></span>                                                | <span data-ttu-id="02693-120">Описание</span><span class="sxs-lookup"><span data-stu-id="02693-120">Description</span></span>                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="02693-121">Обзор</span><span class="sxs-lookup"><span data-stu-id="02693-121">Overview</span></span>](about-system-restore.md)<br/>      | <span data-ttu-id="02693-122">Общие сведения о том, как работает восстановление системы.</span><span class="sxs-lookup"><span data-stu-id="02693-122">An overview of how System Restore works.</span></span><br/>                            |
| [<span data-ttu-id="02693-123">Ссылки</span><span class="sxs-lookup"><span data-stu-id="02693-123">Reference</span></span>](system-restore-reference.md)<br/> | <span data-ttu-id="02693-124">Документация по функциям, структурам и классам восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="02693-124">Documentation of System Restore functions, structures, and classes.</span></span><br/> |
| [<span data-ttu-id="02693-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="02693-125">Samples</span></span>](using-system-restore.md)<br/>       | <span data-ttu-id="02693-126">Пример программы, написанной на языке C.</span><span class="sxs-lookup"><span data-stu-id="02693-126">A sample program written in C.</span></span><br/>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="02693-127">См. также</span><span class="sxs-lookup"><span data-stu-id="02693-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02693-128">WMI</span><span class="sxs-lookup"><span data-stu-id="02693-128">WMI</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

