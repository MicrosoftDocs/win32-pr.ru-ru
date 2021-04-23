---
description: Объект отчета с данными датчика содержит данные датчика.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: Объект отчета с данными датчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d43753aa28be5cd20c85b7e65bf4c7516d4c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998879"
---
# <a name="the-sensor-data-report-object"></a><span data-ttu-id="f8641-103">Объект отчета с данными датчика</span><span class="sxs-lookup"><span data-stu-id="f8641-103">The Sensor Data Report Object</span></span>

<span data-ttu-id="f8641-104">Объект отчета с данными датчика содержит данные датчика.</span><span class="sxs-lookup"><span data-stu-id="f8641-104">The sensor data report object contains sensor data.</span></span>

<span data-ttu-id="f8641-105">Чтобы датчик был полезен, он должен предоставить осмысленные данные.</span><span class="sxs-lookup"><span data-stu-id="f8641-105">For a sensor to be useful, it must provide meaningful data.</span></span> <span data-ttu-id="f8641-106">Количество и частота создания данных меняются от датчика к датчику.</span><span class="sxs-lookup"><span data-stu-id="f8641-106">The amount and frequency of data generation varies from sensor to sensor.</span></span> <span data-ttu-id="f8641-107">Например, датчик, который определяет, открыта ли дверца, создаст небольшой объем **логических** данных, а датчик движения может постоянно формировать несколько элементов данных.</span><span class="sxs-lookup"><span data-stu-id="f8641-107">For example, a sensor that detects whether a door is open would generate a small amount of **Boolean** data, while a motion sensor might continuously generate multiple data items.</span></span> <span data-ttu-id="f8641-108">Чтобы стандартизировать способ получения данных программой, API датчика использует объект отчета с данными датчика.</span><span class="sxs-lookup"><span data-stu-id="f8641-108">To standardize the way your program receives data, the Sensor API uses the sensor data report object.</span></span>

<span data-ttu-id="f8641-109">Вы можете получить доступ к данным в отчете с данными датчика через интерфейс [**исенсордатарепорт**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) .</span><span class="sxs-lookup"><span data-stu-id="f8641-109">You can access the information in a sensor data report through the [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) interface.</span></span> <span data-ttu-id="f8641-110">Этот интерфейс позволяет извлекать отметку времени отчета о данных, чтобы можно было определить, является ли информация в отчете полезной.</span><span class="sxs-lookup"><span data-stu-id="f8641-110">This interface lets you retrieve the data report's time stamp so that you can determine whether the information in the report is useful.</span></span> <span data-ttu-id="f8641-111">Данные можно получить двумя способами: как значение отдельного поля данных или как набор значений.</span><span class="sxs-lookup"><span data-stu-id="f8641-111">You can retrieve the data itself in two ways: as an individual data field value or as a set of values.</span></span> <span data-ttu-id="f8641-112">Чтобы получить данные в виде отдельного значения, вызовите метод [**жетсенсорвалуе**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) .</span><span class="sxs-lookup"><span data-stu-id="f8641-112">To retrieve data as an individual value, call the [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) method.</span></span> <span data-ttu-id="f8641-113">Чтобы получить несколько значений, вызовите метод [**жетсенсорвалуес**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) .</span><span class="sxs-lookup"><span data-stu-id="f8641-113">To retrieve multiple values, call the [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) method.</span></span>

<span data-ttu-id="f8641-114">Укажите тип данных или полей данных, которые необходимо получить из отчета, используя константу **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="f8641-114">You specify the type of data, or data fields, that you want to retrieve from the report by using a **PROPERTYKEY** constant.</span></span> <span data-ttu-id="f8641-115">Ключи свойств для полей данных типов стандартных датчиков определяются в sensors. h.</span><span class="sxs-lookup"><span data-stu-id="f8641-115">Property keys for data fields of common sensor types are defined in Sensors.h.</span></span>

 

 
