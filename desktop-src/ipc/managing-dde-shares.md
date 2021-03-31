---
description: Сетевой DDE предоставляет функции, позволяющие удалять общую папку, получать или задавать сведения о ресурсах или перечислять общие папки.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Управление общими ресурсами DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350952"
---
# <a name="managing-dde-shares"></a><span data-ttu-id="6ee1e-103">Управление общими ресурсами DDE</span><span class="sxs-lookup"><span data-stu-id="6ee1e-103">Managing DDE Shares</span></span>

<span data-ttu-id="6ee1e-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="6ee1e-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="6ee1e-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="6ee1e-106">Сетевой DDE предоставляет функции, позволяющие удалять общую папку, получать или задавать сведения о ресурсах или перечислять общие папки.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-106">Network DDE provides functions that allow you to delete a share, get or set share information, or enumerate shares.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ee1e-107">Задача</span><span class="sxs-lookup"><span data-stu-id="6ee1e-107">Task</span></span></th>
<th><span data-ttu-id="6ee1e-108">Процедура</span><span class="sxs-lookup"><span data-stu-id="6ee1e-108">Procedure</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ee1e-109">Удаление общего ресурса DDE</span><span class="sxs-lookup"><span data-stu-id="6ee1e-109">Delete a DDE share</span></span></td>
<td><span data-ttu-id="6ee1e-110">Используйте функцию <a href="nddesharedel.md"><strong>нддешаредел</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6ee1e-110">Use the <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ee1e-111">Получение сведений об общем ресурсе DDE</span><span class="sxs-lookup"><span data-stu-id="6ee1e-111">Get DDE share information</span></span></td>
<td><span data-ttu-id="6ee1e-112">Используйте функцию <a href="nddesharegetinfo.md"><strong>нддешарежетинфо</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6ee1e-112">Use the <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ee1e-113">Задать сведения об общем ресурсе DDE</span><span class="sxs-lookup"><span data-stu-id="6ee1e-113">Set DDE share information</span></span></td>
<td><span data-ttu-id="6ee1e-114">Используйте функцию <a href="nddesharesetinfo.md"><strong>нддешаресетинфо</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6ee1e-114">Use the <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ee1e-115">Перечисление общих ресурсов DDE</span><span class="sxs-lookup"><span data-stu-id="6ee1e-115">Enumerate DDE shares</span></span></td>
<td><span data-ttu-id="6ee1e-116">Используйте функцию <a href="nddeshareenum.md"><strong>нддешаринум</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6ee1e-116">Use the <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> function.</span></span> <span data-ttu-id="6ee1e-117">Вы также можете перечислить доверенные общие ресурсы DDE с помощью функции <a href="nddetrustedshareenum.md"><strong>нддетрустедшаринум</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6ee1e-117">You can also enumerate the trusted DDE shares by using the <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ee1e-118">Перечисление подключенных пользователей</span><span class="sxs-lookup"><span data-stu-id="6ee1e-118">Enumerate connected users</span></span></td>
<td><span data-ttu-id="6ee1e-119">Используйте функцию <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>нетсессионенум</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6ee1e-119">Use the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ee1e-120">Изменение имени общего ресурса DDE</span><span class="sxs-lookup"><span data-stu-id="6ee1e-120">Change the DDE share name</span></span></td>
<td><span data-ttu-id="6ee1e-121">Удалите старую общую папку и создайте новую.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-121">Delete the old share and create a new share.</span></span>
<ol>
<li><span data-ttu-id="6ee1e-122">Получите сведения об общем ресурсе с помощью <a href="nddesharegetinfo.md"><strong>нддешарежетинфо</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-122">Retrieve the share information using <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="6ee1e-123">Удалите общую папку с помощью <a href="nddesharedel.md"><strong>нддешаредел</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-123">Remove the share using <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span></span></li>
<li><span data-ttu-id="6ee1e-124">Измените элемент <strong>лпсзшаренаме</strong> структуры <a href="nddeshareinfo-str.md"><strong>нддешареинфо</strong></a> , возвращенной <a href="nddesharegetinfo.md"><strong>нддешарежетинфо</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-124">Change the <strong>lpszShareName</strong> member of the <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure returned by <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="6ee1e-125">Передайте измененную структуру <a href="nddeshareinfo-str.md"><strong>нддешареинфо</strong></a> в <a href="nddeshareadd.md"><strong>нддешареадд</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-125">Pass the modified <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure to <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

