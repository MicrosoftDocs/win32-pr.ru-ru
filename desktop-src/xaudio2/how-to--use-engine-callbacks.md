---
description: Вы можете уведомить код клиента XAudio2 о событиях ядра, зарегистрировав экземпляр класса, реализующего интерфейс IXAudio2EngineCallback с подсистемой XAudio2.
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: 'Руководство: использование обратных вызовов модуля'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adec0efd0625157740488d70be7896688d1176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424013"
---
# <a name="how-to-use-engine-callbacks"></a>Руководство: использование обратных вызовов модуля

Вы можете уведомить код клиента XAudio2 о событиях ядра, зарегистрировав экземпляр класса, реализующего интерфейс [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) с подсистемой XAudio2. Это позволяет коду клиента XAudio2 отследить время обработки звука и перезапустить подсистему в случае возникновения критической ошибки.

## <a name="to-use-an-engine-callback"></a>Использование обратного вызова подсистемы

Следующие шаги регистрируют объект для обработки событий обработчика.

1.  Создайте класс, наследующий от интерфейса [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) .

    Все методы [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) являются исключительно виртуальными и должны быть определены. В этом примере метод является [**IXAudio2EngineCallback:: онкритикалеррор**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), который устанавливает флаг для сигнализации основного цикла игры о том, что произошла критическая ошибка. Остальные методы, [**IXAudio2EngineCallback:: онпроцессингпассстарт**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) и [**IXAudio2EngineCallback:: онпроцессингпассенд**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), являются заглушками в этом примере.

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  Используйте [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) для создания экземпляра подсистемы XAudio2.

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Чтобы зарегистрировать обратный вызов модуля, используйте [**IXAudio2:: регистерфоркаллбаккс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) .

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  Если обратный вызов подсистемы больше не требуется, вызовите [**IXAudio2:: унрегистерфоркаллбаккс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обратные вызовы](callbacks.md)
</dt> <dt>

[Обратные вызовы в XAudio2](xaudio2-callbacks.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Руководство: создание базовой схемы обработки звука](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Руководство: организация звукового потока с диска](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
