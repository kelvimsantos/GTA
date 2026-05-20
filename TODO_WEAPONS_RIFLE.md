# TODO - Rifle-Run.glb animação em cima do boxman (overlay) + não quebrar Idle/Walk

- [ ] Confirmar path do GLB runtime: carregar `build/assets/Rifle-Run.glb` (ou ajustar para onde o asset realmente vai)
- [ ] Implementar no `Character`:
  - [ ] Propriedades para `rifleMixer`, `rifleAction`, `rifleAnimationsLoaded`
  - [ ] Método para carregar `Rifle-Run.glb` via `world`/`LoadingManager` (ou disparar carregamento no spawn)
  - [ ] Método `updateRifleAnimation()` chamado em `Character.update()`
    - [ ] Se `isAiming` e `velocidade > threshold` → tocar rifle run
    - [ ] Se `isAiming` e parado → (se existir clip adequado) ou parar rifle
    - [ ] Se `!isAiming` → parar rifle sem afetar Idle/Walk
- [ ] Ajustar `setAnimation()` para não impedir overlay (preferir não chamar `stopAllAction()` quando rifle overlay estiver ativo)
- [ ] Criar toggle/keys:
  - [ ] Usar `Mouse2` como aiming (botão direito) e manter `Mouse0` atirando
  - [ ] Manter `KeyP` switch_weapon já existente
- [ ] Debug/validação:
  - [ ] logar `gltf.animations[].map(a=>a.name)` ao carregar Rifle-Run.glb
  - [ ] verificar se o bone rig é compatível (retarget necessário se não animar)


