---
description: В этом разделе описаны минимальные шаги, необходимые для воспроизведения ранее загруженных звуковых данных в XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Руководство: воспроизведение звука при помощи XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfa5cb2a7a47b7fb54e6a7e9f098a545b0c630c6c27889d7aa6eff1242121d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082917"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a>Руководство: воспроизведение звука при помощи XAudio2

В этом разделе описаны минимальные шаги, необходимые для воспроизведения ранее загруженных звуковых данных в XAudio2. После инициализации XAudio2 (см. раздел [как инициализировать XAudio2](how-to--initialize-xaudio2.md)) и загрузки звуковых данных (см. раздел как [загружать файлы звуковых данных в XAudio2](how-to--load-audio-data-files-in-xaudio2.md)) можно воспроизвести звук, создав исходный голос и передав ему звуковые данные.

## <a name="to-play-a-sound"></a>Воспроизведение звука

1.  Инициализируйте подсистему XAudio2, выполнив действия, описанные в разделе [инструкции. Инициализация XAudio2](how-to--initialize-xaudio2.md).
2.  Заполните структуру [**\_ буфера**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) [**вавеформатекс**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) и XAUDIO2, выполнив действия, описанные в разделе [как загружать файлы аудиоданных в XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).
    > [!Note]  
    > В зависимости от формата звуковых данных может потребоваться использовать более крупную структуру данных, содержащую структуру [**вавеформатекс**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) вместо **вавеформатекс**. Дополнительные сведения см. на странице справочника по **вавеформатекс** .

     

3.  Создайте исходный голоса, вызвав метод [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) на экземпляре обработчика XAudio2. Формат голоса задается значениями, заданными в структуре [**вавеформатекс**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) .
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  Отправьте [**\_ буфер XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) в исходный голоса с помощью функции [**субмитсаурцебуффер**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > Образец данных аудио, в который все *буферные* точки все еще является владельцем приложения и должен оставаться выделенным и доступным до тех пор, пока воспроизведение звука не прекратится.

     

5.  Используйте функцию [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) для запуска исходного голоса. Так как все XAudio2ные голоса отправляют свои выходные данные на основной голос по умолчанию, звук из исходного голоса автоматически выполняет свои операции с звуковым устройством, выбранным при инициализации. В более сложной звуковой диаграмме исходный голос должен указать голос, на который должны отправляться выходные данные.
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>примечания для приложений магазина Windows

Рекомендуется использовать [Интеллектуальный указатель](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) для управления временем существования объектов XAUDIO2 в безопасном режиме исключения. для приложений магазина Windows можно использовать шаблон смарт-указателя [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) из библиотеки шаблонов среда выполнения Windows C++ (WRL).


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> Перед освобождением объекта [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) убедитесь, что все смарт-указатели на объекты XAUDIO2 полностью освобождены.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[XAudio2 начало работы](getting-started.md)
</dt> <dt>

[Руководство: инициализация XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Руководство: загрузка файлов звуковых данных в XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
