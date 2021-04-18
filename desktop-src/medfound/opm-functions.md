---
description: В выходных данных диспетчера защиты (ОПМ) используются следующие функции.
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Функции ОПМ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711438"
---
# <a name="opm-functions"></a>Функции ОПМ

В [выходных данных диспетчера защиты](output-protection-manager.md) (ОПМ) используются следующие функции.



| Функция                                                                                             | Описание                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**опмжетвидеуутпутфортаржет**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | Возвращает объект вывода видео для целевого объекта VidPN на указанном адаптере.                                                          |
| [**опмжетвидеуутпутсфромхмонитор**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | Создает объект диспетчера выходной защиты (ОПМ) для каждого физического монитора, связанного с определенным маркером **хмонитор** . |
| [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | Создает объект ОПМ для каждого физического монитора, связанного с определенным устройством Direct3D.                                 |



 

Для доступа к функциям в драйвере экрана используются следующие функции ОПМ. Приложения не должны вызывать эти функции.

-   [**конфигуреопмпротектедаутпут**](configureopmprotectedoutput.md)
-   [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md)
-   [**дестройопмпротектедаутпут**](destroyopmprotectedoutput.md)
-   [**Метода getcertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [**жетцертификатесизе**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [**жеткоппкомпатиблеопминформатион**](getcoppcompatibleopminformation.md)
-   [**жетопминформатион**](getopminformation.md)
-   [**жетопмрандомнумбер**](getopmrandomnumber.md)
-   [**жетсугжестедопмпротектедаутпутаррайсизе**](getsuggestedopmprotectedoutputarraysize.md)
-   [**сетопмсигнингкэйандсекуенценумберс**](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по программированию ОПМ](opm-programming-reference.md)
</dt> <dt>

[Диспетчер выходной защиты](output-protection-manager.md)
</dt> </dl>

 

 



