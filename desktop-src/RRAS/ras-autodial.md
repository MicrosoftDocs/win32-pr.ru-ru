---
title: Автонабор номера RAS
description: Функция с именем \ 0034; подключение по умолчанию \ 0034; был добавлен в систему Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- Автонабор номера, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2da449b91dd34165038b8d9f07b73926a943a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672153"
---
# <a name="ras-autodial"></a><span data-ttu-id="f05a3-104">Автонабор номера RAS</span><span class="sxs-lookup"><span data-stu-id="f05a3-104">RAS AutoDial</span></span>

<span data-ttu-id="f05a3-105">В системе Windows XP был добавлен компонент «Подключение по умолчанию».</span><span class="sxs-lookup"><span data-stu-id="f05a3-105">A feature called "default connection" was added to the system in Windows XP.</span></span> <span data-ttu-id="f05a3-106">Если попытка подключения не удалась, система проверяет явное совпадение (для имени Winsock или имени общего ресурса) в базе данных, если это не так, при наличии подключения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f05a3-106">If there is a failed connection attempt, the system checks for an explicit match (for Winsock name or share name) in the database if not, it dials the default connection if there is one.</span></span>

<span data-ttu-id="f05a3-107">**Windows 2000:** Если попытка подключения к сетевому адресу завершается сбоем из-за недоступности узла, функция автоматического набора номера может автоматически запустить операцию подключения удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="f05a3-107">**Windows 2000:** When an attempt to connect to a network address fails because the host cannot be reached, the AutoDial feature can automatically start a dial-up connection operation.</span></span> <span data-ttu-id="f05a3-108">Для этого необходимо выполнить автоматический автонабор номеров для поиска в базе данных сетевых адресов, чтобы найти запись телефонной книги, которую можно использовать для установки подключения.</span><span class="sxs-lookup"><span data-stu-id="f05a3-108">To do this, AutoDial searches its database of network addresses to find a phone-book entry that it can use to establish the connection.</span></span>

<span data-ttu-id="f05a3-109">**Windows NT 4,0:  ** Служба RAS сохраняет базу данных имен Winsock и (или) общих имен, которые были успешно достигнуты при активном подключении удаленного доступа или VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="f05a3-109">**Windows NT 4.0:  ** RAS keeps a database of the Winsock names and/or share names that you have successfully reached while a RAS/VPN connection was active.</span></span> <span data-ttu-id="f05a3-110">Позже, когда попытка подключения к Winsock или общей папке завершается неудачно, система проверяет эту базу данных и предлагает установить сохраненное подключение.</span><span class="sxs-lookup"><span data-stu-id="f05a3-110">Later, when a winsock or share connection attempt fails, the system checks this database and offers to dial the stored connection for you.</span></span>

 

 




