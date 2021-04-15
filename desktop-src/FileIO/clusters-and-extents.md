---
description: 'На кластеры можно ссылаться с двух различных точек зрения: в файле и на томе.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Кластеры и экстенты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683564"
---
# <a name="clusters-and-extents"></a><span data-ttu-id="83b86-103">Кластеры и экстенты</span><span class="sxs-lookup"><span data-stu-id="83b86-103">Clusters and Extents</span></span>

<span data-ttu-id="83b86-104">На кластеры можно ссылаться с двух различных точек зрения: в файле и на томе.</span><span class="sxs-lookup"><span data-stu-id="83b86-104">Clusters may be referred to from two different perspectives: within the file and on the volume.</span></span> <span data-ttu-id="83b86-105">Любой кластер в файле имеет *номер виртуального кластера* (VCN), который является его относительным смещением от начала файла.</span><span class="sxs-lookup"><span data-stu-id="83b86-105">Any cluster in a file has a *virtual cluster number* (VCN), which is its relative offset from the beginning of the file.</span></span> <span data-ttu-id="83b86-106">Например, поиск в два раза больше размера кластера, за которым следует Read, будет возвращать данные, начиная с третьего VCN.</span><span class="sxs-lookup"><span data-stu-id="83b86-106">For example, a seek to twice the size of a cluster, followed by a read, will return data beginning at the third VCN.</span></span> <span data-ttu-id="83b86-107">*Логический номер кластера* (LCN) описывает смещение кластера от какой-либо произвольной точки в томе.</span><span class="sxs-lookup"><span data-stu-id="83b86-107">A *logical cluster number* (LCN) describes the offset of a cluster from some arbitrary point within the volume.</span></span> <span data-ttu-id="83b86-108">Лкнс должен обрабатываться только как порядковый номер или относительное число.</span><span class="sxs-lookup"><span data-stu-id="83b86-108">LCNs should be treated only as ordinal, or relative, numbers.</span></span> <span data-ttu-id="83b86-109">Нет гарантированного сопоставления логических кластеров с секторами физических жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="83b86-109">There is no guaranteed mapping of logical clusters to physical hard disk drive sectors.</span></span>

<span data-ttu-id="83b86-110">*Экстент* — это запуск непрерывных кластеров.</span><span class="sxs-lookup"><span data-stu-id="83b86-110">An *extent* is a run of contiguous clusters.</span></span> <span data-ttu-id="83b86-111">Например, предположим, что файл, состоящий из 30 кластеров, записан в двух экстентах.</span><span class="sxs-lookup"><span data-stu-id="83b86-111">For example, suppose a file consisting of 30 clusters is recorded in two extents.</span></span> <span data-ttu-id="83b86-112">Первый экстент может состоять из пяти непрерывных кластеров, а остальные 25 кластеров.</span><span class="sxs-lookup"><span data-stu-id="83b86-112">The first extent might consist of five contiguous clusters, the other of the remaining 25 clusters.</span></span>

<span data-ttu-id="83b86-113">Никакая связь с диском любого экстента не гарантируется в любом другом экстенте.</span><span class="sxs-lookup"><span data-stu-id="83b86-113">There is no guarantee of any relationship on the disk of any extent to any other extent.</span></span> <span data-ttu-id="83b86-114">Например, первый экстент может иметь более высокий уровень LCN, чем последующий экстент.</span><span class="sxs-lookup"><span data-stu-id="83b86-114">For example, the first extent may be at a higher LCN than a subsequent extent.</span></span>

 

 



