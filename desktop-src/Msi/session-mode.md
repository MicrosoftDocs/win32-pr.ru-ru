---
description: Это свойство Mode объекта Session. Это значение, представляющее назначенный флаг режима для текущего сеанса установки. Большинство флагов режима доступны только для чтения извне, но также можно установить несколько заданных флагов.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Свойство Session. Mode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: f081859db789601f2c41bf95d65c377fba8d51f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679945"
---
# <a name="sessionmode-property"></a><span data-ttu-id="ba61d-105">Свойство Session. Mode</span><span class="sxs-lookup"><span data-stu-id="ba61d-105">Session.Mode property</span></span>

<span data-ttu-id="ba61d-106">Это свойство **mode** объекта [**Session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ba61d-106">This is the **Mode** property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="ba61d-107">Это значение, представляющее назначенный флаг режима для текущего сеанса установки.</span><span class="sxs-lookup"><span data-stu-id="ba61d-107">This property is a value representing the designated mode flag for the current install session.</span></span> <span data-ttu-id="ba61d-108">Большинство флагов режима доступны только для чтения извне, но также можно установить несколько заданных флагов.</span><span class="sxs-lookup"><span data-stu-id="ba61d-108">Most of the mode flags are read-only externally, but a few specified flags may be set as well.</span></span>

<span data-ttu-id="ba61d-109">Функция [**мсижетмоде**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) возвращает логическое значение true или false, указывающее, задано ли в настоящий момент конкретное свойство, переданное в функцию (true) или не задано (false).</span><span class="sxs-lookup"><span data-stu-id="ba61d-109">The [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function returns a Boolean TRUE or FALSE, indicating whether the specific property passed into the function is currently set (TRUE) or not set (FALSE).</span></span>

<span data-ttu-id="ba61d-110">Обратите внимание, что не все значения *флага* режима выполнения доступны при вызове свойства **mode** из отложенного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="ba61d-110">Note that not all the run mode values of *flag* are available when calling the **Mode** property from a deferred custom action.</span></span> <span data-ttu-id="ba61d-111">Дополнительные сведения см. в разделе [Получение контекстных сведений для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="ba61d-111">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="ba61d-112">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ba61d-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba61d-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba61d-113">Syntax</span></span>


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a><span data-ttu-id="ba61d-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ba61d-114">Property value</span></span>

<span data-ttu-id="ba61d-115">Обязательное целочисленное значение для флага.</span><span class="sxs-lookup"><span data-stu-id="ba61d-115">Required integer value for the flag.</span></span> <span data-ttu-id="ba61d-116">Должна быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="ba61d-116">Must be one of the following:</span></span>



| <span data-ttu-id="ba61d-117">Имя флага</span><span class="sxs-lookup"><span data-stu-id="ba61d-117">Flag name</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="ba61d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ba61d-118">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <span data-ttu-id="ba61d-119"><dt>**мсирунмодеадмин**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="ba61d-120">Установка в режиме администрирования, в противном случае установка продукта.</span><span class="sxs-lookup"><span data-stu-id="ba61d-120">Administrative mode install, else product install.</span></span><br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <span data-ttu-id="ba61d-121"><dt>**мсирунмодеадвертисе**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="ba61d-122">Режим объявления установки.</span><span class="sxs-lookup"><span data-stu-id="ba61d-122">Advertise mode of install.</span></span><br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <span data-ttu-id="ba61d-123"><dt>**мсирунмодемаинтенанце**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="ba61d-124">База данных режима обслуживания загружена.</span><span class="sxs-lookup"><span data-stu-id="ba61d-124">Maintenance mode database loaded.</span></span><br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <span data-ttu-id="ba61d-125"><dt>**мсирунмодероллбаккенаблед**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="ba61d-126">Откат включен.</span><span class="sxs-lookup"><span data-stu-id="ba61d-126">Rollback is enabled.</span></span><br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <span data-ttu-id="ba61d-127"><dt>**мсирунмоделоженаблед**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="ba61d-128">Файл журнала активен.</span><span class="sxs-lookup"><span data-stu-id="ba61d-128">Log file is active.</span></span><br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <span data-ttu-id="ba61d-129"><dt>**мсирунмодеоператионс**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span></span> </dl>                          | <span data-ttu-id="ba61d-130">Выполнение операций или постановка в очередь.</span><span class="sxs-lookup"><span data-stu-id="ba61d-130">Executing or spooling operations.</span></span><br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <span data-ttu-id="ba61d-131"><dt>**мсирунмодеребутатенд**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span></span> </dl>                      | <span data-ttu-id="ba61d-132">Требуется перезагрузка (Устанавливаемая).</span><span class="sxs-lookup"><span data-stu-id="ba61d-132">Reboot is needed (settable).</span></span><br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <span data-ttu-id="ba61d-133"><dt>**мсирунмодеребутнов**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span></span> </dl>                              | <span data-ttu-id="ba61d-134">Для продолжения установки требуется перезагрузка (Устанавливаемая).</span><span class="sxs-lookup"><span data-stu-id="ba61d-134">Reboot is needed to continue installation (settable).</span></span><br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <span data-ttu-id="ba61d-135"><dt>**мсирунмодекабинет**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span></span> </dl>                                      | <span data-ttu-id="ba61d-136">Установка файлов из ящиков и файлов с помощью таблицы Media.</span><span class="sxs-lookup"><span data-stu-id="ba61d-136">Installing files from cabinets and files using Media table.</span></span><br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <span data-ttu-id="ba61d-137"><dt>**мсирунмодесаурцешортнамес**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="ba61d-138">Исходные файлы используют только короткие имена файлов.</span><span class="sxs-lookup"><span data-stu-id="ba61d-138">Source files use only short file names.</span></span><br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <span data-ttu-id="ba61d-139"><dt>**мсирунмодетаржетшортнамес**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="ba61d-140">В качестве целевых файлов следует использовать только короткие имена файлов.</span><span class="sxs-lookup"><span data-stu-id="ba61d-140">Target files are to use only short file names.</span></span><br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <span data-ttu-id="ba61d-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span></span> </dl>                             | <span data-ttu-id="ba61d-142">Операционная система — Windows 98/95.</span><span class="sxs-lookup"><span data-stu-id="ba61d-142">Operating system is Windows 98/95.</span></span><br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <span data-ttu-id="ba61d-143"><dt>**мсирунмодезавенаблед**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span></span> </dl>                         | <span data-ttu-id="ba61d-144">Операционная система поддерживает рекламу продуктов.</span><span class="sxs-lookup"><span data-stu-id="ba61d-144">Operating system supports advertising of products.</span></span><br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <span data-ttu-id="ba61d-145"><dt>**мсирунмодесчедулед**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span></span> </dl>                             | <span data-ttu-id="ba61d-146">Отложенное [настраиваемое действие](custom-actions.md) , вызываемое из установки выполнения скрипта.</span><span class="sxs-lookup"><span data-stu-id="ba61d-146">Deferred [custom action](custom-actions.md) called from install script execution.</span></span><br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <span data-ttu-id="ba61d-147"><dt>**мсирунмодероллбакк**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="ba61d-148">Отложенное [настраиваемое действие](custom-actions.md) , вызываемое из скрипта выполнения отката.</span><span class="sxs-lookup"><span data-stu-id="ba61d-148">Deferred [custom action](custom-actions.md) called from rollback execution script.</span></span><br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <span data-ttu-id="ba61d-149"><dt>**мсирунмодекоммит**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="ba61d-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span></span> </dl>                                         | <span data-ttu-id="ba61d-150">Отложенное [настраиваемое действие](custom-actions.md) , вызываемое из скрипта выполнения фиксации.</span><span class="sxs-lookup"><span data-stu-id="ba61d-150">Deferred [custom action](custom-actions.md) called from commit execution script.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="ba61d-151">Требования</span><span class="sxs-lookup"><span data-stu-id="ba61d-151">Requirements</span></span>



| <span data-ttu-id="ba61d-152">Требование</span><span class="sxs-lookup"><span data-stu-id="ba61d-152">Requirement</span></span> | <span data-ttu-id="ba61d-153">Значение</span><span class="sxs-lookup"><span data-stu-id="ba61d-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba61d-154">Версия</span><span class="sxs-lookup"><span data-stu-id="ba61d-154">Version</span></span><br/> | <span data-ttu-id="ba61d-155">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ba61d-155">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ba61d-156">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ba61d-156">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ba61d-157">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba61d-157">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



 

 




