---
description: В этом разделе показано, как сгруппировать XAudio2 методы, чтобы они вступили в силу одновременно.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 'Руководство: группировка звуковых методов как набора операций'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f5c1d27e33db4c0f7910761a7be574b72e9ac7aaa91b14329fa003792860d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082928"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a>Руководство: группировка звуковых методов как набора операций

В этом разделе показано, как сгруппировать XAudio2 методы, чтобы они вступили в силу одновременно.

## <a name="to-group-audio-methods-as-an-operation-set"></a>Группировка звуковых методов в виде набора операций

1.  Объявите счетчик глобального набора операций.

    Счетчик [набора операций](operation-sets.md) гарантирует уникальность каждого набора операций.

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  Увеличьте значение глобального счетчика.

    Каждый раз при отправке нового [набора операций](operation-sets.md)глобальный счетчик должен увеличиваться, чтобы гарантировать уникальность каждого набора.

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  Сгруппируйте вызовы методов, задав параметры их [набора операций](operation-sets.md) .

4.  Задайте для параметров [набора операций](operation-sets.md) текущее значение глобального счетчика.

    В этом случае четыре вызова [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) группируются как один [набор операций](operation-sets.md). Группирование вызовов приводит к тому, что все четыре звуковых сигнала запускаются в точно такое же время.

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  Запуск [набора операций](operation-sets.md).

    После вызова всех методов в наборе запустите набор, вызвав [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) с текущим значением глобального счетчика.

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Наборы операций](operation-sets.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Наборы операций XAudio2](xaudio2-operation-sets.md)
</dt> </dl>

 

 
