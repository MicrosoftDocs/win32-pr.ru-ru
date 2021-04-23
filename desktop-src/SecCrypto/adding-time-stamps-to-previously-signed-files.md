---
description: Метки времени обычно включаются, когда файл подписывается с помощью средства SignTool с параметром-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Добавление меток времени в ранее подписанные файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105664953"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a><span data-ttu-id="4cca4-103">Добавление меток времени в ранее подписанные файлы</span><span class="sxs-lookup"><span data-stu-id="4cca4-103">Adding Time Stamps to Previously Signed Files</span></span>

<span data-ttu-id="4cca4-104">Метки времени обычно включаются, когда файл подписывается с помощью средства SignTool с параметром **-t** .</span><span class="sxs-lookup"><span data-stu-id="4cca4-104">Time stamps are normally included when a file is signed using SignTool with the **-t** option.</span></span> <span data-ttu-id="4cca4-105">Кроме того, метки времени можно добавлять к файлам, которые были подписаны без отметки времени.</span><span class="sxs-lookup"><span data-stu-id="4cca4-105">In addition, time stamps can be added to files that were signed without a time stamp.</span></span> <span data-ttu-id="4cca4-106">Следующая команда добавляет отметку времени к ранее подписанному файлу:</span><span class="sxs-lookup"><span data-stu-id="4cca4-106">The following command adds a time stamp to a previously signed file:</span></span>

<span data-ttu-id="4cca4-107">**Метка времени SignTool-t HTTPS: \/ /timestamp.digicert.com *MyControl.exe***</span><span class="sxs-lookup"><span data-stu-id="4cca4-107">**signtool timestamp -t https:\//timestamp.digicert.com *MyControl.exe***</span></span>

> [!Note]  
> <span data-ttu-id="4cca4-108">Файл, к которому отметок времени, должен быть ранее подписан.</span><span class="sxs-lookup"><span data-stu-id="4cca4-108">The file to be time stamped must have previously been signed.</span></span>

 

<span data-ttu-id="4cca4-109">Дополнительные сведения о SignTool см. в разделе [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="4cca4-109">For more information about SignTool, see [SignTool](signtool.md).</span></span>

 

 



