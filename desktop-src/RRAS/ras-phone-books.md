---
title: Телефонные книги RAS
description: Телефонные книги предоставляют стандартный способ для получения и указания сведений, необходимых диспетчеру подключений удаленного доступа для установления удаленного подключения.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Телефонные книги, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068073"
---
# <a name="ras-phone-books"></a><span data-ttu-id="10291-104">Телефонные книги RAS</span><span class="sxs-lookup"><span data-stu-id="10291-104">RAS Phone Books</span></span>

<span data-ttu-id="10291-105">Телефонные книги предоставляют стандартный способ для получения и указания сведений, необходимых диспетчеру подключений удаленного доступа для установления удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="10291-105">Phone books provide a standard way to collect and specify the information that the Remote Access Connection Manager needs to establish a remote connection.</span></span> <span data-ttu-id="10291-106">Телефонные книги связывают имена записей со сведениями, такими как номера телефонов, COM-порты и параметры модема.</span><span class="sxs-lookup"><span data-stu-id="10291-106">Phone books associate entry names with information such as phone numbers, COM ports, and modem settings.</span></span> <span data-ttu-id="10291-107">Каждая запись телефонной книги содержит сведения, необходимые для установления подключения RAS.</span><span class="sxs-lookup"><span data-stu-id="10291-107">Each phone-book entry contains the information needed to establish a RAS connection.</span></span>

<span data-ttu-id="10291-108">Телефонные книги хранятся в файлах телефонной книги, которые являются текстовыми файлами, содержащими имена записей и связанные с ними сведения.</span><span class="sxs-lookup"><span data-stu-id="10291-108">Phone books are stored in phone-book files, which are text files that contain the entry names and associated information.</span></span> <span data-ttu-id="10291-109">Служба RAS создает файл телефонной книги с именем RASPHONE. PBK.</span><span class="sxs-lookup"><span data-stu-id="10291-109">RAS creates a phone-book file called RASPHONE.PBK.</span></span> <span data-ttu-id="10291-110">Пользователь может использовать диалоговое окно основного **удаленного доступа к сети** для создания личных файлов телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="10291-110">The user can use the main **Dial-Up Networking** dialog box to create personal phone-book files.</span></span> <span data-ttu-id="10291-111">API RAS в настоящее время не поддерживает создание файла телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="10291-111">The RAS API does not currently provide support for creating a phone-book file.</span></span> <span data-ttu-id="10291-112">Некоторые функции RAS, например функция [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , имеют параметр, задающий файл телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="10291-112">Some RAS functions, such as the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function, have a parameter that specifies a phone-book file.</span></span> <span data-ttu-id="10291-113">Если вызывающий объект не указывает файл телефонной книги, функция использует файл телефонной книги по умолчанию, выбранный пользователем на странице свойств **предпочтения пользователей** диалогового окна **коммутируемая сеть** .</span><span class="sxs-lookup"><span data-stu-id="10291-113">If the caller does not specify a phone-book file, the function uses the default phone-book file, which is the one selected by the user in the **User Preferences** property sheet of the **Dial-Up Networking** dialog box.</span></span>

<span data-ttu-id="10291-114">Windows NT 4,0 предоставляет функции [**расфонебукдлг**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) и [**расентридлг**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) , которые ОТОБРАЖАЮТ встроенный пользовательский интерфейс RAS, позволяющий пользователям работать с телефонными книгами и записями в телефонной книге.</span><span class="sxs-lookup"><span data-stu-id="10291-114">Windows NT 4.0 provides the [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) and [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) functions that display the built-in RAS user interface that enable users to work with phone books and phone-book entries.</span></span>

<span data-ttu-id="10291-115">**Windows 95:** Удаленный доступ к сети хранит записи телефонной книги в реестре, а не в файле телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="10291-115">**Windows 95:** Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.</span></span> <span data-ttu-id="10291-116">Windows 95 не поддерживает личные телефонные книги или функции, которые отображают встроенные диалоговые окна RAS.</span><span class="sxs-lookup"><span data-stu-id="10291-116">Windows 95 does not support personal phone-book files or functions that display the built-in RAS dialog boxes.</span></span>

 

 




