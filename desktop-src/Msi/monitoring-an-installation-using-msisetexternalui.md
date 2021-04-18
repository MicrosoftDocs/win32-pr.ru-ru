---
description: Авторы пакетов могут отслеживать внутренние установщик Windows сообщения посредством создания исполняемого приложения, которое содержит и обработчик обратного вызова, чтобы получить сообщения и функции для запуска установки.
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: Мониторинг установки с помощью Мсисетекстерналуи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06cc461845a6db1fab4ede22581093c46c0e76e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664418"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a><span data-ttu-id="0ab5c-103">Мониторинг установки с помощью Мсисетекстерналуи</span><span class="sxs-lookup"><span data-stu-id="0ab5c-103">Monitoring an Installation Using MsiSetExternalUI</span></span>

<span data-ttu-id="0ab5c-104">Авторы пакетов могут отслеживать внутренние установщик Windows сообщения посредством создания исполняемого приложения, которое содержит и обработчик обратного вызова, чтобы получить сообщения и функции для запуска установки.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-104">Package authors can monitor internal Windows Installer messages through the creation of an executable application that contains both a callback handler to receive the messages and functionality to initiate an installation.</span></span>

<span data-ttu-id="0ab5c-105">Обработчик обратного вызова соответствует \_ прототипу обработчика инсталлуи, а указатель на этот обработчик обратного вызова передается в [**мсисетекстерналуи**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia).</span><span class="sxs-lookup"><span data-stu-id="0ab5c-105">The callback handler conforms to the INSTALLUI\_HANDLER prototype, and a pointer to this callback handler is passed to [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia).</span></span> <span data-ttu-id="0ab5c-106">После того как установка была инициирована вызовом [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), сообщения установки перехватываются обработчиком обратного вызова, и автор пакета может выборочно отобразить или пропустить какие-либо из этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-106">Once the installation has been initiated by a call to [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), installation messages are trapped by the callback handler and the package author can selectively display or ignore any or all of these messages.</span></span>

<span data-ttu-id="0ab5c-107">Дополнительные сведения см. в статьях [Обработка сообщений о ходе выполнения с помощью мсисетекстерналуи](handling-progress-messages-using-msisetexternalui.md), [возвращение значений из внешнего обработчика пользовательского интерфейса](returning-values-from-an-external-user-interface-handler.md)и [анализ установщик Windows сообщений](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="0ab5c-107">For more information, see [Handling Progress Messages Using MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [Returning Values from an External User Interface Handler](returning-values-from-an-external-user-interface-handler.md), and [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="0ab5c-108">Дополнительные сведения об использовании внешнего обработчика на основе записей см. в разделе [мониторинг установки с помощью мсисетекстерналуирекорд](monitoring-an-installation-using-msisetexternaluirecord.md).</span><span class="sxs-lookup"><span data-stu-id="0ab5c-108">For more information about using a record-based external handler, see [Monitoring an Installation Using MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).</span></span>

 

 



