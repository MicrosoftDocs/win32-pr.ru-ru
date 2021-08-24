---
description: 'Для методов IWbemServices:: ExecMethod или Ексекмесодасинк требуется \_ \_ системный класс Parameters в качестве контейнера в пинпарамс, если у метода, который они выполняют, есть входные аргументы.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Создание объектов параметров в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa97753eab9554e402a91cfce72a6435d44298b6b68a83de96fd4beccd83bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244524"
---
# <a name="creating-parameters-objects-in-c"></a>Создание объектов параметров в C++

Для методов [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) или [**ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) требуется системный класс [**\_ \_ Parameters**](--parameters.md) в качестве контейнера в *пинпарамс* , если у метода, который они выполняют, есть входные аргументы.

В следующей процедуре описывается создание экземпляра системного класса [**\_ \_ Parameters**](--parameters.md) для хранения сведений о параметрах.

**Создание экземпляра \_ \_ параметров**

1.  Определите путь к классу для класса, содержащего определение метода.
2.  С помощью пути к классу и аргумента [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , переданного из метода [**Ивбемпровидеринит:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), вызовите [**ивбемклассобжект:: Method**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) , чтобы получить классы входных и выходных параметров.

    Метод метода [**WebMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) возвращает указатель [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) для доступа к каждому из этих классов.

3.  С помощью указателя [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) для выходного класса вызовите [**Ивбемклассобжект:: спавнинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) , чтобы создать экземпляр класса.
4.  Заполните экземпляр класса, задав свойства, соответствующие выходным значениям, и, если имеется возвращаемое значение для метода, свойство [ReturnValue](creating-a-method.md) .
5.  Передайте экземпляр [**\_ \_ параметров**](--parameters.md) обратно вызывающему объекту через метод [**ивбемобжектсинк:: обозначают**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

После того как поставщик метода определит, что входные параметры верны, метод, на который указывает *стрмесоднаме* , может по-прежнему пройти или завершиться неудачно. Некоторые поставщики методов порождают второй поток для реализации метода, чтобы фактический успех или неудача выполнения метода был передан вызывающему объекту через [**ивбемобжектсинк:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Обратите внимание, что **ивбемобжектсинк:: SetStatus** не получает код возврата метода поставщика. Однако он получает код возврата фактического механизма возврата вызовов, и его удобно использовать только для проверки того, что вызов произошел, или что его не удалось выполнить по механическим причинам.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Вызов метода](calling-a-method.md)
</dt> <dt>

[**Ивбемкаллресулт:: Жетресултобжект**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices:: Ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



