---
description: XAudio2 инициализируется для воспроизведения звука путем создания экземпляра механизма XAudio2 и создания основного голоса.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: 'Руководство: инициализация XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb55425c92e6d28a2689fb388869bbf42339d14bec3550e3f9e17798c1af68f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962733"
---
# <a name="how-to-initialize-xaudio2"></a>Руководство: инициализация XAudio2

XAudio2 инициализируется для воспроизведения звука путем создания экземпляра механизма XAudio2 и создания основного голоса.

**Инициализация XAudio2**

1.  Убедитесь, что инициализирован COM. для приложения магазина Windows это выполняется как часть инициализации среда выполнения Windows. В противном случае используйте [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  Используйте функцию [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) для создания экземпляра подсистемы XAudio2.

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Используйте метод [**креатемастерингвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) для создания основного голоса.

    Голоса в главном канале инкапсулирует звуковое устройство. Он является конечным местом для всех аудио, проходящих через аудио граф.

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>примечания для приложений магазина Windows

Рекомендуется использовать [Интеллектуальный указатель](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) для управления временем существования объектов XAUDIO2 в безопасном режиме исключения. для приложений магазина Windows можно использовать шаблон смарт-указателя [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) из библиотеки шаблонов среда выполнения Windows C++ (WRL).


```C++
Microsoft::WRL::ComPtr<IXAudio2> XAudio2;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &XAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    throw Platform::Exception::CreateException(hr);

IXAudio2MasteringVoice* pMasterVoice = nullptr;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
    return hr;
```



> [!Note]  
> Перед освобождением объекта [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) убедитесь, что все дочерние объекты XAUDIO2 полностью освобождены.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[XAudio2 начало работы](getting-started.md)
</dt> <dt>

[Руководство: загрузка файлов звуковых данных в XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[Руководство: воспроизведение звука при помощи XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
