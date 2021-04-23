---
description: HKLM \\ программное обеспечение \\ \\ клиента Microsoft MSSQLSERVER \\ .
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: SsASnoversion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072421"
---
# <a name="connectto"></a><span data-ttu-id="adc18-103">SsASnoversion</span><span class="sxs-lookup"><span data-stu-id="adc18-103">ConnectTo</span></span>

<span data-ttu-id="adc18-104">**HKLM \\ программное обеспечение \\ \\ клиента Microsoft MSSQLSERVER \\**</span><span class="sxs-lookup"><span data-stu-id="adc18-104">**HKLM\\SOFTWARE\\Microsoft\\MSSQLServer\\Client**</span></span>

## <a name="description"></a><span data-ttu-id="adc18-105">Описание</span><span class="sxs-lookup"><span data-stu-id="adc18-105">Description</span></span>

<span data-ttu-id="adc18-106">В подразделе **ssASnoversion** хранятся сведения о соединении для клиентов под управлением Windows, подключающихся к экземплярам компонента ядра СУБД Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="adc18-106">The **ConnectTo** subkey stores connection information for Windows-based clients that connect to instances of the Microsoft SQL Server database engine.</span></span> <span data-ttu-id="adc18-107">Записи реестра в этом подразделе имеют тип данных REG \_ SZ, а их значения указывают Net-Library, используемые для подключения к экземпляру, а также любые параметры, относящиеся к сети.</span><span class="sxs-lookup"><span data-stu-id="adc18-107">Registry entries in this subkey are of data type REG\_SZ, and their values specify the Net-Library to use for connecting to the instance, as well as any network-specific parameters.</span></span>

<span data-ttu-id="adc18-108">Сведения о подключении, хранящиеся в этом подразделе, считываются поставщиком OLE DB для SQL Server, драйвером SQL Server ODBC или библиотекой динамической компоновки SQL Server DB-Library (DLL).</span><span class="sxs-lookup"><span data-stu-id="adc18-108">The connection information stored in this subkey is read by the OLE DB Provider for SQL Server, the SQL Server ODBC driver, or the SQL Server DB-Library dynamic-link library (DLL).</span></span>

## <a name="change-method"></a><span data-ttu-id="adc18-109">Изменение метода</span><span class="sxs-lookup"><span data-stu-id="adc18-109">Change Method</span></span>

<span data-ttu-id="adc18-110">Не следует изменять записи в этом подразделе с помощью редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="adc18-110">You should not modify entries in this subkey by using the registry editor.</span></span> <span data-ttu-id="adc18-111">Чтобы настроить имя сервера и сведения о соединении, используйте служебную программу клиента SQL Server Network.</span><span class="sxs-lookup"><span data-stu-id="adc18-111">Use the SQL Server Client Network Utility to configure server name and connection information.</span></span> <span data-ttu-id="adc18-112">Дополнительные сведения см. в справке программы SQL Server Client Network.</span><span class="sxs-lookup"><span data-stu-id="adc18-112">See SQL Server Client Network Utility Help for further instructions.</span></span>

## <a name="notes"></a><span data-ttu-id="adc18-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="adc18-113">Notes</span></span>

-   <span data-ttu-id="adc18-114">Подключ **ssASnoversion** используется поставщиком OLE DB для SQL Server, драйвером SQL Server ODBC и SQL Server DB-Library DLL.</span><span class="sxs-lookup"><span data-stu-id="adc18-114">The **ConnectTo** subkey is used by the OLE DB Provider for SQL Server, the SQL Server ODBC Driver, and the SQL Server DB-Library DLL.</span></span> <span data-ttu-id="adc18-115">Записи в этом подразделе указывают, какие Net-Library вызывают эти компоненты API доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="adc18-115">Entries in this subkey identify which Net-Library these data access application programming interface (API) components call.</span></span>
-   <span data-ttu-id="adc18-116">Net-Libraries являются компонентами SQL Server, которые защищают компоненты API доступа к данным из подробных сведений об использовании различных методов межпроцессного взаимодействия (IPC) для взаимодействия с экземпляром ядра СУБД SQL Server.</span><span class="sxs-lookup"><span data-stu-id="adc18-116">Net-Libraries are SQL Server components that shield the data access API components from the details of using different Interprocess Communication (IPC) methods to communicate with an instancess of the SQL Server database engine.</span></span>
-   <span data-ttu-id="adc18-117">Неправильное обновление подраздела **ssASnoversion** может препятствовать успешному подключению приложений к экземпляру компонента ядра СУБД SQL Server.</span><span class="sxs-lookup"><span data-stu-id="adc18-117">Improperly updating the **ConnectTo** subkey might prevent applications from successfully connecting to an instance of the SQL Server database engine.</span></span>

 

 



