---
description: Координатор распределенных транзакций (DTC) позволяет выполнять распределенные транзакции или транзакции под управлением нескольких диспетчеров ресурсов в одной или нескольких системах. Для решения KTM и DTC тесно работают вместе.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Взаимодействие с другими функциями Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683737"
---
# <a name="interoperability-with-other-windows-features"></a><span data-ttu-id="904fc-104">Взаимодействие с другими функциями Windows</span><span class="sxs-lookup"><span data-stu-id="904fc-104">Interoperability With Other Windows Features</span></span>

<span data-ttu-id="904fc-105">[Координатор распределенных транзакций](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) позволяет выполнять *распределенные транзакции* или транзакции под управлением нескольких диспетчеров ресурсов в одной или нескольких системах.</span><span class="sxs-lookup"><span data-stu-id="904fc-105">The [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) enables *distributed transactions*, or transactions that are under the control of multiple resource managers on one or more systems.</span></span> <span data-ttu-id="904fc-106">Для решения KTM и DTC тесно работают вместе.</span><span class="sxs-lookup"><span data-stu-id="904fc-106">KTM and DTC work closely together to accomplish this.</span></span>

<span data-ttu-id="904fc-107">COM+ предоставляет декларативную модель для транзакционного программирования.</span><span class="sxs-lookup"><span data-stu-id="904fc-107">COM+ exposes a declarative model for transactional programming.</span></span> <span data-ttu-id="904fc-108">Иными словами, программист объявляет экстент, в котором объект может использовать преимущества транзакций, а среда выполнения COM+ управляет транзакциями от имени объекта.</span><span class="sxs-lookup"><span data-stu-id="904fc-108">In other words, the programmer declares the extent to which an object can take advantage of transactions, and the COM+ runtime manages the transactions on the object's behalf.</span></span> <span data-ttu-id="904fc-109">Например, объект может быть объявлен для участия в транзакции только в том случае, если он уже существует, чтобы требовать транзакцию (она создается, если она еще не существует), чтобы требовать новую транзакцию (она создается независимо от того, существует ли она) или не является транзакционной.</span><span class="sxs-lookup"><span data-stu-id="904fc-109">For example, an object can be declared to participate in a transaction only if one already exists, to require a transaction (one is created if it does not already exist), to require a new transaction (one is created regardless of whether one already exists), or is not transactional.</span></span> <span data-ttu-id="904fc-110">Эти декларативно управляемые транзакции автоматически используются для подключений к базе данных, созданных объектами COM+, которые выполняются в контексте транзакции.</span><span class="sxs-lookup"><span data-stu-id="904fc-110">These declaratively-managed transactions are automatically used on database connections created by COM+ objects that are executing in the context of a transaction.</span></span>

 

 
