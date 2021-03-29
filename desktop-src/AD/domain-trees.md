---
title: Деревья доменов
description: Доменное дерево состоит из нескольких доменов, которые совместно используют общую схему и конфигурацию, образуя непрерывное пространство имен.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- Active Directory дерева доменов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252792"
---
# <a name="domain-trees"></a><span data-ttu-id="6b87e-104">Деревья доменов</span><span class="sxs-lookup"><span data-stu-id="6b87e-104">Domain Trees</span></span>

<span data-ttu-id="6b87e-105">*Доменное дерево* состоит из нескольких доменов, которые совместно используют общую схему и конфигурацию, образуя непрерывное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="6b87e-105">A *domain tree* is made up of several domains that share a common schema and configuration, forming a contiguous namespace.</span></span> <span data-ttu-id="6b87e-106">Домены в дереве также связываются вместе отношениями доверия.</span><span class="sxs-lookup"><span data-stu-id="6b87e-106">Domains in a tree are also linked together by trust relationships.</span></span> <span data-ttu-id="6b87e-107">Active Directory — это набор из одного или нескольких деревьев.</span><span class="sxs-lookup"><span data-stu-id="6b87e-107">Active Directory is a set of one or more trees.</span></span>

<span data-ttu-id="6b87e-108">Деревья можно просмотреть двумя способами.</span><span class="sxs-lookup"><span data-stu-id="6b87e-108">Trees can be viewed two ways.</span></span> <span data-ttu-id="6b87e-109">Одно из представлений — отношения доверия между доменами.</span><span class="sxs-lookup"><span data-stu-id="6b87e-109">One view is the trust relationships between domains.</span></span> <span data-ttu-id="6b87e-110">Другое представление — это пространство имен дерева доменов.</span><span class="sxs-lookup"><span data-stu-id="6b87e-110">The other view is the namespace of the domain tree.</span></span>

## <a name="viewing-trust-relationships"></a><span data-ttu-id="6b87e-111">Просмотр отношений доверия</span><span class="sxs-lookup"><span data-stu-id="6b87e-111">Viewing Trust Relationships</span></span>

<span data-ttu-id="6b87e-112">Вы можете нарисовать схему дерева доменов на основе отдельных доменов и существующих отношений доверия.</span><span class="sxs-lookup"><span data-stu-id="6b87e-112">You can draw a diagram of a domain tree based on the individual domains and the existing trust relationship.</span></span>

<span data-ttu-id="6b87e-113">Windows 2000 устанавливает отношения доверия между доменами на основе протокола безопасности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="6b87e-113">Windows 2000 establishes trust relationships between domains based on the Kerberos security protocol.</span></span> <span data-ttu-id="6b87e-114">Доверие Kerberos является транзитивным и иерархическим, если домен A доверяет домену B, а домен б доверяет домену C, а домен A доверяет домену C.</span><span class="sxs-lookup"><span data-stu-id="6b87e-114">Kerberos trust is transitive and hierarchical—if domain A trusts domain B, and domain B trusts domain C, then domain A trusts domain C.</span></span>

![доверительное отношение дерева доменов](images/domain-trust.png)

## <a name="viewing-the-namespace"></a><span data-ttu-id="6b87e-116">Просмотр пространства имен</span><span class="sxs-lookup"><span data-stu-id="6b87e-116">Viewing the Namespace</span></span>

<span data-ttu-id="6b87e-117">Можно также нарисовать схему дерева доменов на основе пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6b87e-117">You can also draw a diagram of a domain tree based on the namespace.</span></span> <span data-ttu-id="6b87e-118">Различающееся имя объекта можно определить, следуя пути вверх по иерархии пространства имен дерева доменов.</span><span class="sxs-lookup"><span data-stu-id="6b87e-118">You can determine an object's distinguished name by following the path up the hierarchy of the domain tree namespace.</span></span> <span data-ttu-id="6b87e-119">Это представление полезно для группирования объектов в логическую иерархию.</span><span class="sxs-lookup"><span data-stu-id="6b87e-119">This view is useful for grouping objects into a logical hierarchy.</span></span> <span data-ttu-id="6b87e-120">Главным преимуществом непрерывного пространства имен является то, что глубокий поиск из корня пространства имен выполняет поиск всей иерархии.</span><span class="sxs-lookup"><span data-stu-id="6b87e-120">The chief advantage of a contiguous namespace is that a deep search from the root of the namespace searches the entire hierarchy.</span></span>

![дерево доменов пространства имен](images/namespace.png)

 

 




