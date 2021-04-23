---
description: Магазины "Соседние пользователи"
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Магазины "Соседние пользователи"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911312"
---
# <a name="people-near-me-stores"></a><span data-ttu-id="06c34-103">Магазины "Соседние пользователи"</span><span class="sxs-lookup"><span data-stu-id="06c34-103">People Near Me Stores</span></span>

<span data-ttu-id="06c34-104">Приложения, поддерживающие [соседние пользователи](about-people-near-me.md) (PNM), могут использовать следующие хранилища данных:</span><span class="sxs-lookup"><span data-stu-id="06c34-104">Applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following data stores:</span></span>

### <a name="windows-address-book"></a><span data-ttu-id="06c34-105">Адресная книга Windows</span><span class="sxs-lookup"><span data-stu-id="06c34-105">Windows Address Book</span></span>

<span data-ttu-id="06c34-106">В адресной книге Windows хранятся сведения о контактах и их цифровых сертификатах.</span><span class="sxs-lookup"><span data-stu-id="06c34-106">The Windows Address Book stores information on contacts and their digital certificates.</span></span> <span data-ttu-id="06c34-107">Контакт "**я**", представляющий текущего пользователя, также хранится в адресной книге Windows.</span><span class="sxs-lookup"><span data-stu-id="06c34-107">The '**Me**' contact, representing the currently logged in user, is also stored in the Windows Address Book.</span></span>

### <a name="certificate-store"></a><span data-ttu-id="06c34-108">Хранилище сертификатов</span><span class="sxs-lookup"><span data-stu-id="06c34-108">Certificate Store</span></span>

<span data-ttu-id="06c34-109">Хранилище сертификатов содержит самозаверяющий сертификат для контакта "**Me**".</span><span class="sxs-lookup"><span data-stu-id="06c34-109">The Certificate Store contains the self-signed certificate for the '**Me**' contact.</span></span>

### <a name="application-store"></a><span data-ttu-id="06c34-110">Магазин приложений</span><span class="sxs-lookup"><span data-stu-id="06c34-110">Application Store</span></span>

<span data-ttu-id="06c34-111">Установщик приложения регистрирует приложение в PNM во время процесса установки.</span><span class="sxs-lookup"><span data-stu-id="06c34-111">An application installer registers an application with PNM during the installation process.</span></span> <span data-ttu-id="06c34-112">Это объекты, которые могут быть просмотрены другими пользователями при попытке подключиться к пользователю с помощью общего приложения, например компьютерной игры.</span><span class="sxs-lookup"><span data-stu-id="06c34-112">These are the objects that can be searched for by other users when attempting to connect to a user with a common application, such as a computer game.</span></span> <span data-ttu-id="06c34-113">Для каждого приложения магазин приложений содержит имя приложения, глобальный уникальный идентификатор (GUID), область приложения, описание и путь к исполняемому файлу программы.</span><span class="sxs-lookup"><span data-stu-id="06c34-113">For each application, the Application Store contains the name of the application, a globally unique identifier (GUID), a scope of the application, a description, and a path to the executable file of the program.</span></span> <span data-ttu-id="06c34-114">Области приложения можно присвоить значение None (не объявлено), соседних пользователей (объявленных в локальной подсети), контакты (объявленные только для контактов) или все (объявленные в локальной подсети и для контактов).</span><span class="sxs-lookup"><span data-stu-id="06c34-114">The scope of an application can be set to None (not advertised), People Near Me (advertised on the local subnet), Contacts (advertised just for contacts), or All (advertised on the local subnet and for contacts).</span></span> <span data-ttu-id="06c34-115">Магазин приложений находится в реестре Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="06c34-115">The Application Store is located in the Windows Vista registry.</span></span>

 

 



