---
title: Системмонитор Склдсннаме, свойство
description: Возвращает или задает имя источника данных ODBC (DSN).
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Сисмон свойство Склдсннаме
- Свойство Склдсннаме Сисмон, интерфейс Системмонитор
- Интерфейс Системмонитор Сисмон, свойство Склдсннаме
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414701"
---
# <a name="systemmonitorsqldsnname-property"></a><span data-ttu-id="e13e5-106">Свойство Системмонитор:: Склдсннаме</span><span class="sxs-lookup"><span data-stu-id="e13e5-106">SystemMonitor::SqlDsnName property</span></span>

<span data-ttu-id="e13e5-107">Возвращает или задает имя источника данных ODBC (DSN).</span><span class="sxs-lookup"><span data-stu-id="e13e5-107">Retrieves or sets the ODBC data source name (DSN).</span></span>

## <a name="syntax"></a><span data-ttu-id="e13e5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e13e5-108">Syntax</span></span>


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a><span data-ttu-id="e13e5-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e13e5-109">Property value</span></span>

<span data-ttu-id="e13e5-110">Имя источника данных ODBC, указывающее на базу данных, содержащую правильные таблицы Perfmon.</span><span class="sxs-lookup"><span data-stu-id="e13e5-110">ODBC data source name that points to a database that contains the correct Perfmon tables.</span></span> <span data-ttu-id="e13e5-111">Формат — SQL: DSN.</span><span class="sxs-lookup"><span data-stu-id="e13e5-111">The format is SQL:DSN.</span></span>

## <a name="remarks"></a><span data-ttu-id="e13e5-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e13e5-112">Remarks</span></span>

<span data-ttu-id="e13e5-113">Для создания файла журнала SQL необходимо использовать оснастку MMC Perfmon. msc.</span><span class="sxs-lookup"><span data-stu-id="e13e5-113">You must use the Perfmon.msc MMC snap-in to generate the SQL log file.</span></span> <span data-ttu-id="e13e5-114">Журналы счетчиков находятся в разделе **журналы и оповещения производительности**.</span><span class="sxs-lookup"><span data-stu-id="e13e5-114">The counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="e13e5-115">Чтобы указать журнал SQL, щелкните правой кнопкой мыши созданный файл журнала и выберите в меню пункт **Свойства** .</span><span class="sxs-lookup"><span data-stu-id="e13e5-115">To specify an SQL log, right-click the log file you created and select **Properties** from the menu.</span></span> <span data-ttu-id="e13e5-116">На странице свойств **файлы журнала** выберите **база данных SQL** в раскрывающемся списке **Тип файла журнала** .</span><span class="sxs-lookup"><span data-stu-id="e13e5-116">On the **Log Files** property page, select **SQL Database** from the **Log file type** drop-down list box.</span></span>

<span data-ttu-id="e13e5-117">**До Windows Vista:** Нельзя изменить это свойство, если для [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) задано значение [**DataSourceTypeConstants.sysмонскллог**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="e13e5-117">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="e13e5-118">Сначала необходимо указать имя, а затем задать **системмонитор. DataSourceType** в **DataSourceTypeConstants.sysмонскллог**.</span><span class="sxs-lookup"><span data-stu-id="e13e5-118">You must first specify the name and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonSqlLog**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e13e5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e13e5-119">Requirements</span></span>



| <span data-ttu-id="e13e5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e13e5-120">Requirement</span></span> | <span data-ttu-id="e13e5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e13e5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e13e5-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e13e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e13e5-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e13e5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e13e5-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e13e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e13e5-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e13e5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e13e5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e13e5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e13e5-127"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e13e5-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13e5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e13e5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13e5-129">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="e13e5-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="e13e5-130">**Системмонитор. Скллогсетнаме**</span><span class="sxs-lookup"><span data-stu-id="e13e5-130">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





